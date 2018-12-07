---
UID: NE:windows.media.streaming.TransportState
title: TransportState
author: windows-sdk-content
description: Defines the available transport states as defined by the UPnP Guidelines.
old-location: mediastreaming\transportstate.htm
tech.root: mediastreaming
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Last, NoMediaPresent, Paused, Playing, Recording, Stopped, Transitioning, TransportState, TransportState enumeration [Media Streaming API], Unknown, mediastreaming.transportstate, windows/Last, windows/NoMediaPresent, windows/Paused, windows/Playing, windows/Recording, windows/Stopped, windows/Transitioning, windows/TransportState, windows/Unknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)
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
 - windows.media.streaming.h
api_name:
 - TransportState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TransportState enumeration


## -description


Defines the available transport states as defined by the UPnP Guidelines.


## -enum-fields




### -field TransportState_Unknown


### -field TransportState_Stopped


### -field TransportState_Playing


### -field TransportState_Transitioning


### -field TransportState_Paused


### -field TransportState_Recording


### -field TransportState_NoMediaPresent


### -field TransportState_Last




#### - Last

The device’s previous state to the current transport state.


#### - NoMediaPresent

The device’s transport  does not have an URI set for playback.


#### - Paused

The device’s transport  is in a paused state.


#### - Playing

The device’s transport  is in a playing state.


#### - Recording

The device’s transport  is in a recording state.


#### - Stopped

The device’s transport  is in a stopped state.


#### - Transitioning

The device’s transport  is in a transitioning state which will result in another state value.


#### - Unknown

Erroneous device state.

