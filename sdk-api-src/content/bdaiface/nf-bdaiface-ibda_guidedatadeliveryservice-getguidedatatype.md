---
UID: NF:bdaiface.IBDA_GuideDataDeliveryService.GetGuideDataType
title: IBDA_GuideDataDeliveryService::GetGuideDataType (bdaiface.h)
description: Gets the format UUID for the data that is retrieved on this service.
helpviewer_keywords: ["CLSID_PBDA_GDDS_DATA_TYPE","GetGuideDataType","GetGuideDataType method [Microsoft TV Technologies]","GetGuideDataType method [Microsoft TV Technologies]","IBDA_GuideDataDeliveryService interface","IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies]","GetGuideDataType method","IBDA_GuideDataDeliveryService.GetGuideDataType","IBDA_GuideDataDeliveryService::GetGuideDataType","bdaiface/IBDA_GuideDataDeliveryService::GetGuideDataType","mstv.ibda_guidedatadeliveryservice_getguidedatatype"]
old-location: mstv\ibda_guidedatadeliveryservice_getguidedatatype.htm
tech.root: mstv
ms.assetid: 74370ba8-2104-41f9-aa02-02b6790236da
ms.date: 12/05/2018
ms.keywords: CLSID_PBDA_GDDS_DATA_TYPE, GetGuideDataType, GetGuideDataType method [Microsoft TV Technologies], GetGuideDataType method [Microsoft TV Technologies],IBDA_GuideDataDeliveryService interface, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],GetGuideDataType method, IBDA_GuideDataDeliveryService.GetGuideDataType, IBDA_GuideDataDeliveryService::GetGuideDataType, bdaiface/IBDA_GuideDataDeliveryService::GetGuideDataType, mstv.ibda_guidedatadeliveryservice_getguidedatatype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_GuideDataDeliveryService::GetGuideDataType
 - bdaiface/IBDA_GuideDataDeliveryService::GetGuideDataType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_GuideDataDeliveryService.GetGuideDataType
---

# IBDA_GuideDataDeliveryService::GetGuideDataType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_guidedatadeliveryservice">IBDA_GuideDataDeliveryService</a>