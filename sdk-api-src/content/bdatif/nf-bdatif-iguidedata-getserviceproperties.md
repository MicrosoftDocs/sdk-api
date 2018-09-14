---
UID: NF:bdatif.IGuideData.GetServiceProperties
title: IGuideData::GetServiceProperties
author: windows-sdk-content
description: The GetServiceProperties method retrieves the properties for a specified service.
old-location: mstv\iguidedata_getserviceproperties.htm
tech.root: MSTV
ms.assetid: 28be3bb7-b76a-44a3-892c-2aade5dbe255
ms.author: windowssdkdev
ms.date: 08/30/2018
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

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd694997(v=VS.85).aspx">ITuneRequest</a> interface of a valid tune request. Call the <a href="https://msdn.microsoft.com/en-us/library/Dd694117(v=VS.85).aspx">IGuideData::GetServices</a> method to get a list of tune requests.


### -param ppEnumProperties [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/en-us/library/Dd693993(v=VS.85).aspx">IEnumGuideDataProperties</a> interface pointer. Use this interface to enumerate the properties. The caller must release the interface.


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
 

The method fails if the TIF has not received the service information from the PSI tables in the transport stream. The client should implement the <a href="https://msdn.microsoft.com/en-us/library/Dd694099(v=VS.85).aspx">IGuideDataEvent</a> interface and wait for the <a href="https://msdn.microsoft.com/en-us/library/Dd694105(v=VS.85).aspx">IGuideDataEvent::ServiceChanged</a> event to be fired.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694098(v=VS.85).aspx">IGuideData Interface</a>
 

 

