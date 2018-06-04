---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

