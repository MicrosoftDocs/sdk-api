---
UID: NF:bdaiface.IBDA_EventingService.CompleteEvent
title: IBDA_EventingService::CompleteEvent (bdaiface.h)
description: Notifies the media transform device (MTD) when the media sink device (MSD) completes an event.
helpviewer_keywords: ["CompleteEvent","CompleteEvent method [Microsoft TV Technologies]","CompleteEvent method [Microsoft TV Technologies]","IBDA_EventingService interface","IBDA_EventingService interface [Microsoft TV Technologies]","CompleteEvent method","IBDA_EventingService.CompleteEvent","IBDA_EventingService::CompleteEvent","bdaiface/IBDA_EventingService::CompleteEvent","mstv.ibda_eventingservice_completeevent"]
old-location: mstv\ibda_eventingservice_completeevent.htm
tech.root: mstv
ms.assetid: 399530a7-5a02-485e-aa5e-6b3ddb7f3d54
ms.date: 12/05/2018
ms.keywords: CompleteEvent, CompleteEvent method [Microsoft TV Technologies], CompleteEvent method [Microsoft TV Technologies],IBDA_EventingService interface, IBDA_EventingService interface [Microsoft TV Technologies],CompleteEvent method, IBDA_EventingService.CompleteEvent, IBDA_EventingService::CompleteEvent, bdaiface/IBDA_EventingService::CompleteEvent, mstv.ibda_eventingservice_completeevent
f1_keywords:
- bdaiface/IBDA_EventingService.CompleteEvent
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
- IBDA_EventingService.CompleteEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_EventingService::CompleteEvent


## -description


Notifies the media transform device (MTD) when the media sink device (MSD) completes an event.


## -parameters




### -param ulEventID [in]

The identifier of the event.


### -param ulEventResult [in]

The result code of the event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_eventingservice">IBDA_EventingService</a>
 

 

