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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

