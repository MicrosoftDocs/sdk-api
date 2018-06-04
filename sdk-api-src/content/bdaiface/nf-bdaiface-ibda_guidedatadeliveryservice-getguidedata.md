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

# IBDA_GuideDataDeliveryService::GetGuideData


## -description


Gets the next set of guide data that is available.


## -parameters




### -param pulcbBufferLen [in, out]

Size of the <i>pbBuffer</i> array, in bytes.


### -param pbBuffer [out]

Pointer to a byte array that receives the guide data.


### -param pulGuideDataPercentageProgress [out]

Receives a value from 0 to 100. The value specifies the percent of guide data that was transferred from the media transform device (MTD) to the media sink device (MSD) since the last call to <a href="https://msdn.microsoft.com/e9aee857-237a-4bfd-85c2-3d5850f37ce7">IBDA_GuideDataDeliveryService::RequestGuideDataUpdate</a>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>BDA_E_NO_MORE_DATA</dt>
</dl>
</td>
<td width="60%">
The MTD has no more data to return.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5329f725-e77e-49c2-87f5-f7204d022adc">IBDA_GuideDataDeliveryService</a>
 

 

