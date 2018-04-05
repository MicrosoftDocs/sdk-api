---
UID: NF:wsdhost.IWSDDeviceHost.AddDynamicService
title: IWSDDeviceHost::AddDynamicService method
author: windows-driver-content
description: Registers a service object for incoming requests, but does not add the service to the device host metadata. This is used for transient (dynamic) services.
old-location: ncd\iwsddevicehost_adddynamicservice_method.htm
old-project: WsdApi
ms.assetid: 0ef7760d-39eb-48fe-a7e9-043c2b9ba5a4
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: AddDynamicService method, AddDynamicService method, IWSDDeviceHost interface, AddDynamicService,IWSDDeviceHost.AddDynamicService, IWSDDeviceHost, IWSDDeviceHost interface, AddDynamicService method, IWSDDeviceHost::AddDynamicService, ncd.iwsddevicehost_adddynamicservice_method, wsdhost/IWSDDeviceHost::AddDynamicService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdHost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDDeviceHost.AddDynamicService
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDDeviceHost::AddDynamicService method


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
 

 

