---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWSDDeviceHost::AddDynamicService


## -description


Registers a service object for incoming requests, but does not add the service to the device host metadata. This is used for transient (dynamic) services.


## -parameters




### -param pszServiceId [in]

The ID for the dynamic service. The service ID must be distinct from all the service IDs in the service host metadata and from any other registered dynamic service. The <i>pszServiceId</i> must be a URI.


### -param pszEndpointAddress [in, optional]

An optional URI to use as the endpoint address for this service. If none is specified, the device host will assume the service should be available on all local transport addresses.


### -param pPortType [in, optional]

Reference to a <a href="https://msdn.microsoft.com/ec321771-b3d1-4e7b-b870-009db7c49c6e">WSD_PORT_TYPE</a> structure that specifies the port type. 
May be <b>NULL</b>. Specify only one of <i>pPortType</i> and <i>pPortName</i>.


### -param pPortName [in, optional]

Reference to a <a href="https://msdn.microsoft.com/9dce71d2-700c-4f86-9308-dee6a69010bb">WSDXML_NAME</a> structure that specifies the type of the service, with associating the service with a specified port. Specify only one of <i>pPortType</i> and <i>pPortName</i>.


### -param pAny [in, optional]

Optional reference to an extensible section to be included in the dynamic service metadata.


### -param pService [in, optional]

 Optional reference to a host service object to register.


## -returns



Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszServiceId</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of <i>pszServiceId</i> or <i>pszEndpointAddress</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or both <i>pPortType</i> and <i>pPortName</i> are specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed. It may have failed because the host has not been initialized, or the service specified by <i>pszServiceId</i> could not be found. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a> to initialize a device host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



When this method is called, the device adds a reference to the service object and calls its methods in response to request messages addressed to the service. Call the <a href="https://msdn.microsoft.com/45c314d3-966b-4b90-ab23-fec2a8e4bc0f">RemoveDynamicService</a> method on the device host to release its reference to the service and stop calling methods on the service.






## -see-also




<a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a>
 

 

