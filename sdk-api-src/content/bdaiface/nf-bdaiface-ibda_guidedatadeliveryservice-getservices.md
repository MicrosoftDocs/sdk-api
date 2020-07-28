---
UID: NF:bdaiface.IBDA_GuideDataDeliveryService.GetServices
title: IBDA_GuideDataDeliveryService::GetServices (bdaiface.h)
description: Gets a list of services that are available on the the media transform device (MTD).
helpviewer_keywords: ["GetServices","GetServices method [Microsoft TV Technologies]","GetServices method [Microsoft TV Technologies]","IBDA_GuideDataDeliveryService interface","IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies]","GetServices method","IBDA_GuideDataDeliveryService.GetServices","IBDA_GuideDataDeliveryService::GetServices","bdaiface/IBDA_GuideDataDeliveryService::GetServices","mstv.ibda_guidedatadeliveryservice_getservices"]
old-location: mstv\ibda_guidedatadeliveryservice_getservices.htm
tech.root: mstv
ms.assetid: 82133fc5-0f42-4b24-abf6-bc46e72650ac
ms.date: 12/05/2018
ms.keywords: GetServices, GetServices method [Microsoft TV Technologies], GetServices method [Microsoft TV Technologies],IBDA_GuideDataDeliveryService interface, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],GetServices method, IBDA_GuideDataDeliveryService.GetServices, IBDA_GuideDataDeliveryService::GetServices, bdaiface/IBDA_GuideDataDeliveryService::GetServices, mstv.ibda_guidedatadeliveryservice_getservices
f1_keywords:
- bdaiface/IBDA_GuideDataDeliveryService.GetServices
dev_langs:
- c++
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
- IBDA_GuideDataDeliveryService.GetServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_GuideDataDeliveryService::GetServices


## -description


Gets a list of services that are available on the the media transform device (MTD).


## -parameters




### -param pulcbBufferLen [in, out]

On input, specifies the size of the <i>pbBuffer</i> array, in bytes. On output, receives the size of the data that was written to the <i>pbBuffer</i> array.


### -param pbBuffer [out]

Pointer to a byte array that receives a list of service identifiers. A service identifier is a 64-bit value. To translate a service identifier into a tune request, call <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_guidedatadeliveryservice-gettunexmlfromserviceidx">IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_guidedatadeliveryservice">IBDA_GuideDataDeliveryService</a>
 

 

