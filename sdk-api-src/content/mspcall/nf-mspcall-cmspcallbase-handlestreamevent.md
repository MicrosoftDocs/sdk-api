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

# CMSPCallBase::HandleStreamEvent


## -description


The 
<b>HandleStreamEvent</b> method is called by a stream to send an event to TAPI. It fills in the call handle in the event info structure and then calls the PostEvent method on the MSP address object. (Note that this way, events generated on the streams "flow" toward the address object via the call object, with more information filled in at each step. This reduces the amount of state that must be kept in the MSP call and MSP stream objects.)


## -parameters




### -param EventItem

Pointer to 
<a href="https://msdn.microsoft.com/fc99fd05-4d87-4b6e-b2f3-e00ac61ddafc">MSPEVENTITEM</a>, a struct containing a linked list of 
<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>
 

 

