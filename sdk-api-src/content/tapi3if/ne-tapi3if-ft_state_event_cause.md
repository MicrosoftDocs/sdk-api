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

# FT_STATE_EVENT_CAUSE enumeration


## -description


The 
<b>FT_STATE_EVENT_CAUSE</b> enum indicates the type of file terminal event.


## -enum-fields




### -field FTEC_NORMAL

State change in response to a normal API call.


### -field FTEC_END_OF_FILE

Storage EOF reached on playback.


### -field FTEC_READ_ERROR

Storage read error on playback.


### -field FTEC_WRITE_ERROR

Storage write error on the record.


#### - FTEC_MAX_DURATION_REACHED

Maximum duration threshold has been reached on the record.


#### - FTEC_PAUSE_ON_SILENCE_SIGNAL_DETECTED

Woken up from the pause caused by triggering the pause-on-silence threshold because a signal was detected.


#### - FTEC_PAUSE_ON_SILENCE_THRESHOLD_TRIGGERED

The pause-on-silence threshold has been reached.


#### - FTEC_STOP_ON_SILENCE_THRESHOLD_TRIGGERED

The stop-on-silence threshold has been reached.


## -see-also




<a href="https://msdn.microsoft.com/90594778-712e-4d26-9fe5-cb5cfd240359">ITFileTerminalEvent::get_Cause</a>
 

 

