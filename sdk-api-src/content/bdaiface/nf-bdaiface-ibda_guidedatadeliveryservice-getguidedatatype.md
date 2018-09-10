---
UID: NF:bdaiface.IBDA_GuideDataDeliveryService.GetGuideDataType
title: IBDA_GuideDataDeliveryService::GetGuideDataType
author: windows-sdk-content
description: Gets the format UUID for the data that is retrieved on this service.
old-location: mstv\ibda_guidedatadeliveryservice_getguidedatatype.htm
tech.root: mstv
ms.assetid: 74370ba8-2104-41f9-aa02-02b6790236da
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CLSID_PBDA_GDDS_DATA_TYPE, GetGuideDataType, GetGuideDataType method [Microsoft TV Technologies], GetGuideDataType method [Microsoft TV Technologies],IBDA_GuideDataDeliveryService interface, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],GetGuideDataType method, IBDA_GuideDataDeliveryService.GetGuideDataType, IBDA_GuideDataDeliveryService::GetGuideDataType, bdaiface/IBDA_GuideDataDeliveryService::GetGuideDataType, mstv.ibda_guidedatadeliveryservice_getguidedatatype
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
 - IBDA_GuideDataDeliveryService.GetGuideDataType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_GuideDataDeliveryService::GetGuideDataType


## -description


Gets the format UUID for the data that is retrieved on this service.


## -parameters




### -param pguidDataType [out]

Receives either a UUID that identifies the format of the guide data or the network GUID that the tuner supports for in-band guide purposes. Possible values include the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLSID_PBDA_GDDS_DATA_TYPE"></a><a id="clsid_pbda_gdds_data_type"></a><dl>
<dt><b>CLSID_PBDA_GDDS_DATA_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Protected Broadcast Driver Architecture Service Information (PBDA-SI) format. 

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693368(v=VS.85).aspx">IBDA_GuideDataDeliveryService</a>
 

 

