---
UID: NE:wmp.WMPPlayState
title: WMPPlayState
author: windows-sdk-content
description: The WMPPlayState enumeration type defines the possible operational states of Windows Media Player as it plays a digital media file.
old-location: wmp\wmpplaystate.htm
old-project: WMP
ms.assetid: 15787d18-bc38-4fc7-a920-539d66252035
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WMPPlayState, WMPPlayState enumeration [Windows Media Player], wmp.wmpplaystate, wmp/WMPPlayState, wmp/wmppsBuffering, wmp/wmppsLast, wmp/wmppsMediaEnded, wmp/wmppsPaused, wmp/wmppsPlaying, wmp/wmppsReady, wmp/wmppsReconnecting, wmp/wmppsScanForward, wmp/wmppsScanReverse, wmp/wmppsStopped, wmp/wmppsTransitioning, wmp/wmppsUndefined, wmp/wmppsWaiting, wmppsBuffering, wmppsLast, wmppsMediaEnded, wmppsPaused, wmppsPlaying, wmppsReady, wmppsReconnecting, wmppsScanForward, wmppsScanReverse, wmppsStopped, wmppsTransitioning, wmppsUndefined, wmppsWaiting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WMPPlayState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPPlayState
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMPPlayState enumeration


## -description



The <b>WMPPlayState</b> enumeration type defines the possible operational states of Windows Media Player as it plays a digital media file.




## -enum-fields




### -field wmppsUndefined

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




<a href="https://msdn.microsoft.com/90689fb7-656d-4c06-a0a9-02bbe0e5b5dd">Enumeration Types</a>
 

 

