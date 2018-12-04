---
UID: NF:segment.IMSVidEVREvent.OnUserEvent
title: IMSVidEVREvent::OnUserEvent
author: windows-sdk-content
description: This topic applies to Windows Vista or later.
old-location: mstv\imsvidevrevent_onuserevent.htm
tech.root: mstv
ms.assetid: 2eee9fd9-ed8d-482d-833a-c785d65cbf6a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidEVREvent interface [Microsoft TV Technologies],OnUserEvent method, IMSVidEVREvent.OnUserEvent, IMSVidEVREvent::OnUserEvent, IMSVidEVREventOnUserEvent, OnUserEvent, OnUserEvent method [Microsoft TV Technologies], OnUserEvent method [Microsoft TV Technologies],IMSVidEVREvent interface, mstv.imsvidevrevent_onuserevent, segment/IMSVidEVREvent::OnUserEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidEVREvent.OnUserEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidEVREvent::OnUserEvent


## -description



This topic applies to Windows Vista or later.
        



The <b>OnUserEvent</b> method forwards custom events from the enhanced video renderer (EVR) filter.


## -parameters




### -param lEventCode [in]

Event code.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The purpose of this method is to forward custom events from an EVR presenter to the application through the Video Control.

<ol>
<li>The presenter calls <a href="https://msdn.microsoft.com/331f8d58-c7c6-40dd-88ca-5678c7b8c8f1">IMediaEventSink::Notify</a> on the EVR with an event code of EC_USER or higher. (This range of values is reserved for custom graph events.)</li>
<li>The EVR forwards the event to the Filter Graph Manager.</li>
<li>The Filter Graph Manager forwards the event to the Video Control.</li>
<li>The Video Control forwards the event to the application by calling <b>OnUserEvent</b>.</li>
</ol>
The dispatch identifier (dispid) of this method is <b>dispidUserEvent</b>.




## -see-also




<a href="https://msdn.microsoft.com/70874420-64f2-43c9-b46b-492318ae0852">IMSVidEVREvent</a>
 

 

