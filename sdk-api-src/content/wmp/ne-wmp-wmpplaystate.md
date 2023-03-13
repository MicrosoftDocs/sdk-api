---
UID: NE:wmp.WMPPlayState
title: WMPPlayState (wmp.h)
description: The WMPPlayState enumeration type defines the possible operational states of Windows Media Player as it plays a digital media file.
helpviewer_keywords: ["WMPPlayState","WMPPlayState enumeration [Windows Media Player]","wmp.wmpplaystate","wmp/WMPPlayState","wmp/wmppsBuffering","wmp/wmppsLast","wmp/wmppsMediaEnded","wmp/wmppsPaused","wmp/wmppsPlaying","wmp/wmppsReady","wmp/wmppsReconnecting","wmp/wmppsScanForward","wmp/wmppsScanReverse","wmp/wmppsStopped","wmp/wmppsTransitioning","wmp/wmppsUndefined","wmp/wmppsWaiting","wmppsBuffering","wmppsLast","wmppsMediaEnded","wmppsPaused","wmppsPlaying","wmppsReady","wmppsReconnecting","wmppsScanForward","wmppsScanReverse","wmppsStopped","wmppsTransitioning","wmppsUndefined","wmppsWaiting"]
old-location: wmp\wmpplaystate.htm
tech.root: WMP
ms.assetid: 15787d18-bc38-4fc7-a920-539d66252035
ms.date: 12/05/2018
ms.keywords: WMPPlayState, WMPPlayState enumeration [Windows Media Player], wmp.wmpplaystate, wmp/WMPPlayState, wmp/wmppsBuffering, wmp/wmppsLast, wmp/wmppsMediaEnded, wmp/wmppsPaused, wmp/wmppsPlaying, wmp/wmppsReady, wmp/wmppsReconnecting, wmp/wmppsScanForward, wmp/wmppsScanReverse, wmp/wmppsStopped, wmp/wmppsTransitioning, wmp/wmppsUndefined, wmp/wmppsWaiting, wmppsBuffering, wmppsLast, wmppsMediaEnded, wmppsPaused, wmppsPlaying, wmppsReady, wmppsReconnecting, wmppsScanForward, wmppsScanReverse, wmppsStopped, wmppsTransitioning, wmppsUndefined, wmppsWaiting
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
targetos: Windows
req.typenames: WMPPlayState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPPlayState
 - wmp/WMPPlayState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPPlayState
---

# WMPPlayState enumeration


## -description

The <b>WMPPlayState</b> enumeration type defines the possible operational states of Windows Media Player as it plays a digital media file.

## -enum-fields

### -field wmppsUndefined:0

Windows Media Player is in an undefined state.

### -field wmppsStopped

Playback is stopped.

### -field wmppsPaused

Playback is paused.

### -field wmppsPlaying

Stream is playing.

### -field wmppsScanForward

Stream is scanning forward.

### -field wmppsScanReverse

Stream is scanning backward.

### -field wmppsBuffering

Stream is being buffered.

### -field wmppsWaiting

Waiting for streaming data.

### -field wmppsMediaEnded

The end of the media item has been reached.

### -field wmppsTransitioning

Preparing new media item.

### -field wmppsReady

Ready to begin playing.

### -field wmppsReconnecting

Trying to reconnect for streaming data.

### -field wmppsLast

Last enumerated value. Not a valid state.

## -see-also

<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>
