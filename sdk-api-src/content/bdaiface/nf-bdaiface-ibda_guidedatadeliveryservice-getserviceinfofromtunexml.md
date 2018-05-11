---
UID: NF:bdaiface.IBDA_GuideDataDeliveryService.GetServiceInfoFromTuneXml
title: IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml
author: windows-driver-content
description: Gets service information from an XML tune request.
old-location: mstv\ibda_guidedatadeliveryservice_getserviceinfofromtunexml.htm
old-project: mstv
ms.assetid: 8084e4dd-a5d5-48a0-a052-24310a79df78
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetServiceInfoFromTuneXml, GetServiceInfoFromTuneXml method [Microsoft TV Technologies], GetServiceInfoFromTuneXml method [Microsoft TV Technologies],IBDA_GuideDataDeliveryService interface, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],GetServiceInfoFromTuneXml method, IBDA_GuideDataDeliveryService.GetServiceInfoFromTuneXml, IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml, bdaiface/IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml, mstv.ibda_guidedatadeliveryservice_getserviceinfofromtunexml
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_GuideDataDeliveryService.GetServiceInfoFromTuneXml
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_GuideDataDeliveryService::GetServiceInfoFromTuneXml


## -description


Gets service information from an XML tune request.


## -parameters




### -param bstrTuneXml [in]

The XML tune request. For more information, see <a href="https://msdn.microsoft.com/5f429473-6a48-4298-b8f4-61809604ffbd">IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx</a> or the section on tuning schemas in Part 1 of the Protected Broadcast Driver Architecture (PBDA) specification, which can be downloaded from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


### -param pbstrServiceDescription [out]

Receives an XML string that contains information about the service. The caller must release the string by calling <b>SysFreeString</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5329f725-e77e-49c2-87f5-f7204d022adc">IBDA_GuideDataDeliveryService</a>
 

 

