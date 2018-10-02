---
UID: NF:bdatif.IGuideData.GetServiceProperties
title: IGuideData::GetServiceProperties
author: windows-sdk-content
description: The GetServiceProperties method retrieves the properties for a specified service.
old-location: mstv\iguidedata_getserviceproperties.htm
tech.root: MSTV
ms.assetid: 28be3bb7-b76a-44a3-892c-2aade5dbe255
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetServiceProperties, GetServiceProperties method [Microsoft TV Technologies], GetServiceProperties method [Microsoft TV Technologies],IGuideData interface, IGuideData interface [Microsoft TV Technologies],GetServiceProperties method, IGuideData.GetServiceProperties, IGuideData::GetServiceProperties, IGuideDataGetServiceProperties, bdatif/IGuideData::GetServiceProperties, mstv.iguidedata_getserviceproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideData.GetServiceProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideData::GetServiceProperties


## -description



The <b>GetServiceProperties</b> method retrieves the properties for a specified service.




## -parameters




### -param pTuneRequest [in]

Pointer to the <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface of a valid tune request. Call the <a href="https://msdn.microsoft.com/a3c08812-ed56-440e-a88d-80e20a681695">IGuideData::GetServices</a> method to get a list of tune requests.


### -param ppEnumProperties [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/ae4db426-7e90-4cb6-b53a-2cb7074308fc">IEnumGuideDataProperties</a> interface pointer. Use this interface to enumerate the properties. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The returned collection includes the following properties.

<table>
<tr>
<th>Property
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>Description.ID</td>
<td>The unique identifier for the service.</td>
</tr>
<tr>
<td>Description.Name</td>
<td>Default name to use for this service in the channel lineup.</td>
</tr>
<tr>
<td>Provider.Name</td>
<td>Name of the service provider.</td>
</tr>
<tr>
<td>Provider.NetworkName</td>
<td>Name of the network on which the service is provided.</td>
</tr>
</table>
 

The method fails if the TIF has not received the service information from the PSI tables in the transport stream. The client should implement the <a href="https://msdn.microsoft.com/9da565f2-fbcb-4d71-ae40-7d9821f46630">IGuideDataEvent</a> interface and wait for the <a href="https://msdn.microsoft.com/75387dd8-e0e2-4fae-8c4a-a0b7b06f61b1">IGuideDataEvent::ServiceChanged</a> event to be fired.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3bd27fce-90be-480b-b157-a17beccda068">IGuideData Interface</a>
 

 

