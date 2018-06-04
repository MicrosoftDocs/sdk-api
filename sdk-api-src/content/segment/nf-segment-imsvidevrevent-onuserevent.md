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
 

 

