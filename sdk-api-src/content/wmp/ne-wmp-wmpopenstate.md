---
UID: NE:wmp.WMPOpenState
title: WMPOpenState
author: windows-sdk-content
description: The WMPOpenState enumeration type defines the possible operational states of Windows Media Player as it opens a digital media file.
old-location: wmp\wmpopenstate.htm
old-project: WMP
ms.assetid: 535c8f56-d854-449b-ad50-72e5dd32710a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WMPOpenState, WMPOpenState enumeration [Windows Media Player], wmp.wmpopenstate, wmp/WMPOpenState, wmp/wmposBeginCodecAcquisition, wmp/wmposBeginIndividualization, wmp/wmposBeginLicenseAcquisition, wmp/wmposEndCodecAcquisition, wmp/wmposEndIndividualization, wmp/wmposEndLicenseAcquisition, wmp/wmposMediaChanging, wmp/wmposMediaConnecting, wmp/wmposMediaLoading, wmp/wmposMediaLocating, wmp/wmposMediaOpen, wmp/wmposMediaOpening, wmp/wmposMediaWaiting, wmp/wmposOpeningUnknownURL, wmp/wmposPlaylistChanged, wmp/wmposPlaylistChanging, wmp/wmposPlaylistConnecting, wmp/wmposPlaylistLoading, wmp/wmposPlaylistLocating, wmp/wmposPlaylistOpenNoMedia, wmp/wmposPlaylistOpening, wmp/wmposUndefined, wmposBeginCodecAcquisition, wmposBeginIndividualization, wmposBeginLicenseAcquisition, wmposEndCodecAcquisition, wmposEndIndividualization, wmposEndLicenseAcquisition, wmposMediaChanging, wmposMediaConnecting, wmposMediaLoading, wmposMediaLocating, wmposMediaOpen, wmposMediaOpening, wmposMediaWaiting, wmposOpeningUnknownURL, wmposPlaylistChanged, wmposPlaylistChanging, wmposPlaylistConnecting, wmposPlaylistLoading, wmposPlaylistLocating, wmposPlaylistOpenNoMedia, wmposPlaylistOpening, wmposUndefined
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WMPOpenState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPOpenState
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

