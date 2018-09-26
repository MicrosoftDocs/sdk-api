---
UID: NF:bdaiface.IBDA_GuideDataDeliveryService.GetGuideData
title: IBDA_GuideDataDeliveryService::GetGuideData
author: windows-sdk-content
description: Gets the next set of guide data that is available.
old-location: mstv\ibda_guidedatadeliveryservice_getguidedata.htm
tech.root: MSTV
ms.assetid: c261d20e-3760-4bf9-905b-f5620df4166b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetGuideData, GetGuideData method [Microsoft TV Technologies], GetGuideData method [Microsoft TV Technologies],IBDA_GuideDataDeliveryService interface, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],GetGuideData method, IBDA_GuideDataDeliveryService.GetGuideData, IBDA_GuideDataDeliveryService::GetGuideData, bdaiface/IBDA_GuideDataDeliveryService::GetGuideData, mstv.ibda_guidedatadeliveryservice_getguidedata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - bdaiface.h
api_name:
 - IBDA_GuideDataDeliveryService.GetGuideData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Receives a value from 0 to 100. The value specifies the percent of guide data that was transferred from the media transform device (MTD) to the media sink device (MSD) since the last call to <a href="https://msdn.microsoft.com/en-us/library/Dd693374(v=VS.85).aspx">IBDA_GuideDataDeliveryService::RequestGuideDataUpdate</a>.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd693368(v=VS.85).aspx">IBDA_GuideDataDeliveryService</a>
 

 

