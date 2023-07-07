---
UID: NF:tuner.IESEvents.OnESEventReceived
title: IESEvents::OnESEventReceived (tuner.h)
description: Defines a handler for an event that is derived from the IESEvent interface.
helpviewer_keywords: ["IESEvents interface [Microsoft TV Technologies]","OnESEventReceived method","IESEvents.OnESEventReceived","IESEvents::OnESEventReceived","OnESEventReceived","OnESEventReceived method [Microsoft TV Technologies]","OnESEventReceived method [Microsoft TV Technologies]","IESEvents interface","mstv.iesevents_oneseventreceived","tuner/IESEvents::OnESEventReceived"]
old-location: mstv\iesevents_oneseventreceived.htm
tech.root: mstv
ms.assetid: d715f598-0dd5-4c8c-9f5b-3aaa65768600
ms.date: 12/05/2018
ms.keywords: IESEvents interface [Microsoft TV Technologies],OnESEventReceived method, IESEvents.OnESEventReceived, IESEvents::OnESEventReceived, OnESEventReceived, OnESEventReceived method [Microsoft TV Technologies], OnESEventReceived method [Microsoft TV Technologies],IESEvents interface, mstv.iesevents_oneseventreceived, tuner/IESEvents::OnESEventReceived
f1_keywords:
- tuner/IESEvents.OnESEventReceived
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
- tuner.h
api_name:
- IESEvents.OnESEventReceived
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEvents::OnESEventReceived


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]


Defines a handler for an event that is derived from the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface.
    In a Protected Broadcast Driver Architecture graph, Media Sink Devices that implement the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevents">IESEvents</a> interface use this method to obtain data from Event System events that these devices receive. In this context, <i>Event System events</i> refer to event objects that that implement the <b>IESEvent</b> interface.

If an event originates from a PBDA device, the event object automatically calls the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_eventingservice-completeevent">IBDA_EventingService::CompleteEvent</a> method with the result set in the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iesevent-setcompletionstatus">SetCompletionStatus</a> call at the time it is released.  If the client is a managed application, it should dispose of the event object immediately after it is finished with the event. This disposition ensures that the <b>IBDA_EventingService::CompleteEvent</b> method is called in a timely manner

This method is called from an event service thread that is initialized with multithreaded COM concurrency.  The receiving object must use the multithreaded threading model or the single-threaded model with proper marshaling.


## -parameters




### -param guidEventType [in]

GUID for the type of event being handled.
          


### -param pESEvent [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> object that contains data from the event being handled.
          


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevents">IESEvents</a>
 

 