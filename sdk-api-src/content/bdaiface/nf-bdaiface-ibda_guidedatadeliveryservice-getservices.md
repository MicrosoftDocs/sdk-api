---
UID: NF:bdaiface.IBDA_GuideDataDeliveryService.GetServices
title: IBDA_GuideDataDeliveryService::GetServices
author: windows-sdk-content
description: Gets a list of services that are available on the the media transform device (MTD).
old-location: mstv\ibda_guidedatadeliveryservice_getservices.htm
old-project: mstv
ms.assetid: 82133fc5-0f42-4b24-abf6-bc46e72650ac
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetServices, GetServices method [Microsoft TV Technologies], GetServices method [Microsoft TV Technologies],IBDA_GuideDataDeliveryService interface, IBDA_GuideDataDeliveryService interface [Microsoft TV Technologies],GetServices method, IBDA_GuideDataDeliveryService.GetServices, IBDA_GuideDataDeliveryService::GetServices, bdaiface/IBDA_GuideDataDeliveryService::GetServices, mstv.ibda_guidedatadeliveryservice_getservices
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_GuideDataDeliveryService.GetServices
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_GuideDataDeliveryService::GetServices


## -description


Gets a list of services that are available on the the media transform device (MTD).


## -parameters




### -param pulcbBufferLen [in, out]

On input, specifies the size of the <i>pbBuffer</i> array, in bytes. On output, receives the size of the data that was written to the <i>pbBuffer</i> array.


### -param pbBuffer [out]

Pointer to a byte array that receives a list of service identifiers. A service identifier is a 64-bit value. To translate a service identifier into a tune request, call <a href="https://msdn.microsoft.com/5f429473-6a48-4298-b8f4-61809604ffbd">IBDA_GuideDataDeliveryService::GetTuneXmlFromServiceIdx</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5329f725-e77e-49c2-87f5-f7204d022adc">IBDA_GuideDataDeliveryService</a>
 

 

