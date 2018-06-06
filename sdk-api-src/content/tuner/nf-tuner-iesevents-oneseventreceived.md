---
UID: NF:tuner.IESEvents.OnESEventReceived
title: IESEvents::OnESEventReceived
author: windows-sdk-content
description: Defines a handler for an event that is derived from the IESEvent interface.
old-location: mstv\iesevents_oneseventreceived.htm
old-project: mstv
ms.assetid: d715f598-0dd5-4c8c-9f5b-3aaa65768600
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IESEvents interface [Microsoft TV Technologies],OnESEventReceived method, IESEvents.OnESEventReceived, IESEvents::OnESEventReceived, OnESEventReceived, OnESEventReceived method [Microsoft TV Technologies], OnESEventReceived method [Microsoft TV Technologies],IESEvents interface, mstv.iesevents_oneseventreceived, tuner/IESEvents::OnESEventReceived
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESEvents.OnESEventReceived
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESEvents::OnESEventReceived


## -description


Defines a handler for an event that is derived from the <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a> interface.
    In a Protected Broadcast Driver Architecture graph, Media Sink Devices that implement the <a href="https://msdn.microsoft.com/1921f632-bb3b-4833-aa25-9caa3d65363f">IESEvents</a> interface use this method to obtain data from Event System events that these devices receive. In this context, <i>Event System events</i> refer to event objects that that implement the <b>IESEvent</b> interface.

If an event originates from a PBDA device, the event object automatically calls the <a href="https://msdn.microsoft.com/399530a7-5a02-485e-aa5e-6b3ddb7f3d54">IBDA_EventingService::CompleteEvent</a> method with the result set in the <a href="https://msdn.microsoft.com/2e8d5a94-6fa1-453b-bbd4-396d60bb2aa0">SetCompletionStatus</a> call at the time it is released.  If the client is a managed application, it should dispose of the event object immediately after it is finished with the event. This disposition ensures that the <b>IBDA_EventingService::CompleteEvent</b> method is called in a timely manner

This method is called from an event service thread that is initialized with multithreaded COM concurrency.  The receiving object must use the multithreaded threading model or the single-threaded model with proper marshaling.


## -parameters




### -param guidEventType [in]


            GUID for the type of event being handled.
          


### -param pESEvent [in]


            Pointer to an <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a> object that contains data from the event being handled.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a>



<a href="https://msdn.microsoft.com/1921f632-bb3b-4833-aa25-9caa3d65363f">IESEvents</a>
 

 

