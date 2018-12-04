---
UID: NE:tapi3if.FT_STATE_EVENT_CAUSE
title: FT_STATE_EVENT_CAUSE
author: windows-sdk-content
description: The FT_STATE_EVENT_CAUSE enum indicates the type of file terminal event.
old-location: tapi3\ft_state_event_cause.htm
tech.root: tapi
ms.assetid: dd81fe2d-07ab-404b-8510-52029d67ef9b
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: FTEC_END_OF_FILE, FTEC_MAX_DURATION_REACHED, FTEC_NORMAL, FTEC_PAUSE_ON_SILENCE_SIGNAL_DETECTED, FTEC_PAUSE_ON_SILENCE_THRESHOLD_TRIGGERED, FTEC_READ_ERROR, FTEC_STOP_ON_SILENCE_THRESHOLD_TRIGGERED, FTEC_WRITE_ERROR, FT_STATE_EVENT_CAUSE, FT_STATE_EVENT_CAUSE enumeration [TAPI 2.2], _tapi3_ft_state_event_cause, tapi3.ft_state_event_cause, tapi3if/FTEC_END_OF_FILE, tapi3if/FTEC_MAX_DURATION_REACHED, tapi3if/FTEC_NORMAL, tapi3if/FTEC_PAUSE_ON_SILENCE_SIGNAL_DETECTED, tapi3if/FTEC_PAUSE_ON_SILENCE_THRESHOLD_TRIGGERED, tapi3if/FTEC_READ_ERROR, tapi3if/FTEC_STOP_ON_SILENCE_THRESHOLD_TRIGGERED, tapi3if/FTEC_WRITE_ERROR, tapi3if/FT_STATE_EVENT_CAUSE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - FT_STATE_EVENT_CAUSE
product: Windows
targetos: Windows
req.typenames: FT_STATE_EVENT_CAUSE
req.redist: 
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
 

 

