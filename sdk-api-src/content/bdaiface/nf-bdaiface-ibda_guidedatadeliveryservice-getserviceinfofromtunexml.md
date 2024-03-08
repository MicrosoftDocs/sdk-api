---
UID: NF:bdaiface.IBDA_GuideDataDeliveryService.GetServiceInfoFromTuneXml
title: IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml (bdaiface.h)
description: Gets service information from an XML tune request.
helpviewer_keywords: ["GetServiceInfoFromTuneXml","GetServiceInfoFromTuneXml method [Microsoft TV Technologies]","GetServiceInfoFromTuneXml method [Microsoft TV Technologies]","IBDA_GuideDataDeliveryService interface","IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies]","GetServiceInfoFromTuneXml method","IBDA_GuideDataDeliveryService.GetServiceInfoFromTuneXml","IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml","bdaiface/IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml","mstv.ibda_guidedatadeliveryservice_getserviceinfofromtunexml"]
old-location: mstv\ibda_guidedatadeliveryservice_getserviceinfofromtunexml.htm
tech.root: mstv
ms.assetid: 8084e4dd-a5d5-48a0-a052-24310a79df78
ms.date: 12/05/2018
ms.keywords: GetServiceInfoFromTuneXml, GetServiceInfoFromTuneXml method [Microsoft TV Technologies], GetServiceInfoFromTuneXml method [Microsoft TV Technologies],IBDA_GuideDataDeliveryService interface, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],GetServiceInfoFromTuneXml method, IBDA_GuideDataDeliveryService.GetServiceInfoFromTuneXml, IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml, bdaiface/IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml, mstv.ibda_guidedatadeliveryservice_getserviceinfofromtunexml
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
 - IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml
 - bdaiface/IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml
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
 - IBDA_GuideDataDeliveryService.GetServiceInfoFromTuneXml
---

# IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets service information from an XML tune request.

## -parameters

### -param bstrTuneXml [in]

The XML tune request. For more information, see <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_guidedatadeliveryservice-gettunexmlfromserviceidx">IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx</a>.

### -param pbstrServiceDescription [out]

Receives an XML string that contains information about the service. The caller must release the string by calling <b>SysFreeString</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_guidedatadeliveryservice">IBDA_GuideDataDeliveryService</a>