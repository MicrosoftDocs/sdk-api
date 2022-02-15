---
UID: NE:windows.media.streaming.TransportState
title: TransportState (windows.media.streaming.h)
description: Defines the available transport states as defined by the UPnP Guidelines.
helpviewer_keywords: ["Last","NoMediaPresent","Paused","Playing","Recording","Stopped","Transitioning","TransportState","TransportState enumeration [Media Streaming API]","Unknown","mediastreaming.transportstate","windows/Last","windows/NoMediaPresent","windows/Paused","windows/Playing","windows/Recording","windows/Stopped","windows/Transitioning","windows/TransportState","windows/Unknown"]
old-location: mediastreaming\transportstate.htm
tech.root: mediastreaming
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
ms.date: 12/05/2018
ms.keywords: Last, NoMediaPresent, Paused, Playing, Recording, Stopped, Transitioning, TransportState, TransportState enumeration [Media Streaming API], Unknown, mediastreaming.transportstate, windows/Last, windows/NoMediaPresent, windows/Paused, windows/Playing, windows/Recording, windows/Stopped, windows/Transitioning, windows/TransportState, windows/Unknown
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TransportState
 - windows.media.streaming/TransportState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windows.media.streaming.h
api_name:
 - TransportState
---

# TransportState enumeration


## -description

Defines the available transport states as defined by the UPnP Guidelines.

## -enum-fields

### -field TransportState_Unknown:0

### -field TransportState_Stopped:1

### -field TransportState_Playing:2

### -field TransportState_Transitioning:3

### -field TransportState_Paused:4

### -field TransportState_Recording:5

### -field TransportState_NoMediaPresent:6

### -field TransportState_Last:7

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

