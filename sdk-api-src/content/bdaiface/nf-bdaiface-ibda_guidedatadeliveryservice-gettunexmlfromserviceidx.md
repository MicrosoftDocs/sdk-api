---
UID: NF:bdaiface.IBDA_GuideDataDeliveryService.GetTuneXmlFromServiceIdx
title: IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx (bdaiface.h)
description: Converts a service identifier into an XML tune request.
helpviewer_keywords: ["GetTuneXmlFromServiceIdx","GetTuneXmlFromServiceIdx method [Microsoft TV Technologies]","GetTuneXmlFromServiceIdx method [Microsoft TV Technologies]","IBDA_GuideDataDeliveryService interface","IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies]","GetTuneXmlFromServiceIdx method","IBDA_GuideDataDeliveryService.GetTuneXmlFromServiceIdx","IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx","bdaiface/IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx","mstv.ibda_guidedatadeliveryservice_gettunexmlfromserviceidx"]
old-location: mstv\ibda_guidedatadeliveryservice_gettunexmlfromserviceidx.htm
tech.root: mstv
ms.assetid: 5f429473-6a48-4298-b8f4-61809604ffbd
ms.date: 12/05/2018
ms.keywords: GetTuneXmlFromServiceIdx, GetTuneXmlFromServiceIdx method [Microsoft TV Technologies], GetTuneXmlFromServiceIdx method [Microsoft TV Technologies],IBDA_GuideDataDeliveryService interface, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],GetTuneXmlFromServiceIdx method, IBDA_GuideDataDeliveryService.GetTuneXmlFromServiceIdx, IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx, bdaiface/IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx, mstv.ibda_guidedatadeliveryservice_gettunexmlfromserviceidx
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
 - IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx
 - bdaiface/IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx
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
 - IBDA_GuideDataDeliveryService.GetTuneXmlFromServiceIdx
---

# IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Converts a service identifier into an XML  tune request.

A service identifier (<i>ServiceIdx</i>) is a 64-bit identifier, used in the PBDA EIT guide delivery format. An XML tune request (<i>TuneXml</i>) is an XML string that can be used to tune to the  service.

## -parameters

### -param ul64ServiceIdx [in]

Identifier for the service.

### -param pbstrTuneXml [out]

Receives the XML tune request. The caller must release the string by calling <b>SysFreeString</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_guidedatadeliveryservice">IBDA_GuideDataDeliveryService</a>