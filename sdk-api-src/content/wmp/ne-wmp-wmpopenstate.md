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

# WMPOpenState enumeration


## -description



The <b>WMPOpenState</b> enumeration type defines the possible operational states of Windows Media Player as it opens a digital media file.




## -enum-fields




### -field wmposUndefined

The content source is in an undefined state.


### -field wmposPlaylistChanging

A new playlist is about to be loaded.


### -field wmposPlaylistLocating

Locating the playlist.


### -field wmposPlaylistConnecting

Connecting to the server that is hosting the playlist.


### -field wmposPlaylistLoading

Loading a playlist.


### -field wmposPlaylistOpening

Opening a playlist.


### -field wmposPlaylistOpenNoMedia

Playlist is open.


### -field wmposPlaylistChanged

Playlist has changed.


### -field wmposMediaChanging

New media item is about to be loaded.


### -field wmposMediaLocating

Locating the media item.


### -field wmposMediaConnecting

Connecting to the server that is hosting the media item.


### -field wmposMediaLoading

Loading the media item.


### -field wmposMediaOpening

Opening the media item.


### -field wmposMediaOpen

The media item is open.


### -field wmposBeginCodecAcquisition

Starting codec acquisition.


### -field wmposEndCodecAcquisition

Ending codec acquisition.


### -field wmposBeginLicenseAcquisition

Starting license acquisition.


### -field wmposEndLicenseAcquisition

Ending license acquisition.


### -field wmposBeginIndividualization

Starting individualization.


### -field wmposEndIndividualization

Individualization has ended.


### -field wmposMediaWaiting

Waiting for the media item to open.


### -field wmposOpeningUnknownURL

Opening a URL whose type is unknown.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

