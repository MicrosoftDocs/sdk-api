---
UID: NE:wmp.WMPOpenState
title: WMPOpenState (wmp.h)
description: The WMPOpenState enumeration type defines the possible operational states of Windows Media Player as it opens a digital media file.
helpviewer_keywords: ["WMPOpenState","WMPOpenState enumeration [Windows Media Player]","wmp.wmpopenstate","wmp/WMPOpenState","wmp/wmposBeginCodecAcquisition","wmp/wmposBeginIndividualization","wmp/wmposBeginLicenseAcquisition","wmp/wmposEndCodecAcquisition","wmp/wmposEndIndividualization","wmp/wmposEndLicenseAcquisition","wmp/wmposMediaChanging","wmp/wmposMediaConnecting","wmp/wmposMediaLoading","wmp/wmposMediaLocating","wmp/wmposMediaOpen","wmp/wmposMediaOpening","wmp/wmposMediaWaiting","wmp/wmposOpeningUnknownURL","wmp/wmposPlaylistChanged","wmp/wmposPlaylistChanging","wmp/wmposPlaylistConnecting","wmp/wmposPlaylistLoading","wmp/wmposPlaylistLocating","wmp/wmposPlaylistOpenNoMedia","wmp/wmposPlaylistOpening","wmp/wmposUndefined","wmposBeginCodecAcquisition","wmposBeginIndividualization","wmposBeginLicenseAcquisition","wmposEndCodecAcquisition","wmposEndIndividualization","wmposEndLicenseAcquisition","wmposMediaChanging","wmposMediaConnecting","wmposMediaLoading","wmposMediaLocating","wmposMediaOpen","wmposMediaOpening","wmposMediaWaiting","wmposOpeningUnknownURL","wmposPlaylistChanged","wmposPlaylistChanging","wmposPlaylistConnecting","wmposPlaylistLoading","wmposPlaylistLocating","wmposPlaylistOpenNoMedia","wmposPlaylistOpening","wmposUndefined"]
old-location: wmp\wmpopenstate.htm
tech.root: WMP
ms.assetid: 535c8f56-d854-449b-ad50-72e5dd32710a
ms.date: 12/05/2018
ms.keywords: WMPOpenState, WMPOpenState enumeration [Windows Media Player], wmp.wmpopenstate, wmp/WMPOpenState, wmp/wmposBeginCodecAcquisition, wmp/wmposBeginIndividualization, wmp/wmposBeginLicenseAcquisition, wmp/wmposEndCodecAcquisition, wmp/wmposEndIndividualization, wmp/wmposEndLicenseAcquisition, wmp/wmposMediaChanging, wmp/wmposMediaConnecting, wmp/wmposMediaLoading, wmp/wmposMediaLocating, wmp/wmposMediaOpen, wmp/wmposMediaOpening, wmp/wmposMediaWaiting, wmp/wmposOpeningUnknownURL, wmp/wmposPlaylistChanged, wmp/wmposPlaylistChanging, wmp/wmposPlaylistConnecting, wmp/wmposPlaylistLoading, wmp/wmposPlaylistLocating, wmp/wmposPlaylistOpenNoMedia, wmp/wmposPlaylistOpening, wmp/wmposUndefined, wmposBeginCodecAcquisition, wmposBeginIndividualization, wmposBeginLicenseAcquisition, wmposEndCodecAcquisition, wmposEndIndividualization, wmposEndLicenseAcquisition, wmposMediaChanging, wmposMediaConnecting, wmposMediaLoading, wmposMediaLocating, wmposMediaOpen, wmposMediaOpening, wmposMediaWaiting, wmposOpeningUnknownURL, wmposPlaylistChanged, wmposPlaylistChanging, wmposPlaylistConnecting, wmposPlaylistLoading, wmposPlaylistLocating, wmposPlaylistOpenNoMedia, wmposPlaylistOpening, wmposUndefined
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
req.typenames: WMPOpenState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPOpenState
 - wmp/WMPOpenState
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
 - WMPOpenState
---

# WMPOpenState enumeration


## -description

The <b>WMPOpenState</b> enumeration type defines the possible operational states of Windows Media Player as it opens a digital media file.

## -enum-fields

### -field wmposUndefined:0

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

<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>
