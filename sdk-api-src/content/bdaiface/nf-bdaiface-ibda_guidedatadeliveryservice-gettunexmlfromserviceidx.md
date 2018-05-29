---
UID: NF:bdaiface.IBDA_GuideDataDeliveryService.GetTuneXmlFromServiceIdx
title: IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx
author: windows-sdk-content
description: Converts a service identifier into an XML tune request.
old-location: mstv\ibda_guidedatadeliveryservice_gettunexmlfromserviceidx.htm
old-project: mstv
ms.assetid: 5f429473-6a48-4298-b8f4-61809604ffbd
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetTuneXmlFromServiceIdx, GetTuneXmlFromServiceIdx method [Microsoft TV Technologies], GetTuneXmlFromServiceIdx method [Microsoft TV Technologies],IBDA_GuideDataDeliveryService interface, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],GetTuneXmlFromServiceIdx method, IBDA_GuideDataDeliveryService.GetTuneXmlFromServiceIdx, IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx, bdaiface/IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx, mstv.ibda_guidedatadeliveryservice_gettunexmlfromserviceidx
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_GuideDataDeliveryService.GetTuneXmlFromServiceIdx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx


## -description


Converts a service identifier into an XML  tune request.

A service identifier (<i>ServiceIdx</i>) is a 64-bit identifier, used in the PBDA EIT guide delivery format. An XML tune request (<i>TuneXml</i>) is an XML string that can be used to tune to the  service.


## -parameters




### -param ul64ServiceIdx [in]

Identifier for the service.


### -param pbstrTuneXml [out]

Receives the XML tune request. The caller must release the string by calling <b>SysFreeString</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5329f725-e77e-49c2-87f5-f7204d022adc">IBDA_GuideDataDeliveryService</a>
 

 

