---
UID: NE:wmp.WMPPlaylistChangeEventType
title: WMPPlaylistChangeEventType (wmp.h)
description: The WMPPlaylistChangeEventType enumeration type defines the types of changes that can be made to a playlist.
helpviewer_keywords: ["WMPPlaylistChangeEventType","WMPPlaylistChangeEventType enumeration [Windows Media Player]","wmp.wmpplaylistchangeeventtype","wmp/WMPPlaylistChangeEventType","wmp/wmplcAppend","wmp/wmplcClear","wmp/wmplcDelete","wmp/wmplcInfoChange","wmp/wmplcInsert","wmp/wmplcLast","wmp/wmplcMorph","wmp/wmplcMove","wmp/wmplcNameChange","wmp/wmplcPrivate","wmp/wmplcSort","wmp/wmplcUnknown","wmplcAppend","wmplcClear","wmplcDelete","wmplcInfoChange","wmplcInsert","wmplcLast","wmplcMorph","wmplcMove","wmplcNameChange","wmplcPrivate","wmplcSort","wmplcUnknown"]
old-location: wmp\wmpplaylistchangeeventtype.htm
tech.root: WMP
ms.assetid: ebddaf22-9052-4180-9cc4-75059f9d286c
ms.date: 12/05/2018
ms.keywords: WMPPlaylistChangeEventType, WMPPlaylistChangeEventType enumeration [Windows Media Player], wmp.wmpplaylistchangeeventtype, wmp/WMPPlaylistChangeEventType, wmp/wmplcAppend, wmp/wmplcClear, wmp/wmplcDelete, wmp/wmplcInfoChange, wmp/wmplcInsert, wmp/wmplcLast, wmp/wmplcMorph, wmp/wmplcMove, wmp/wmplcNameChange, wmp/wmplcPrivate, wmp/wmplcSort, wmp/wmplcUnknown, wmplcAppend, wmplcClear, wmplcDelete, wmplcInfoChange, wmplcInsert, wmplcLast, wmplcMorph, wmplcMove, wmplcNameChange, wmplcPrivate, wmplcSort, wmplcUnknown
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
req.typenames: WMPPlaylistChangeEventType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPPlaylistChangeEventType
 - wmp/WMPPlaylistChangeEventType
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
 - WMPPlaylistChangeEventType
---

# WMPPlaylistChangeEventType enumeration


## -description

The <b>WMPPlaylistChangeEventType</b> enumeration type defines the types of changes that can be made to a playlist.

## -enum-fields

### -field wmplcUnknown:0

An unknown change has occurred.

### -field wmplcClear

The playlist has been cleared.

### -field wmplcInfoChange

A playlist attribute has changed value.

### -field wmplcMove

A media item within the playlist has been moved to a new position.

### -field wmplcDelete

A media item has been deleted from the playlist.

### -field wmplcInsert

A media item has been inserted into the playlist.

### -field wmplcAppend

A media item has been appended to the playlist.

### -field wmplcPrivate

Not supported.

### -field wmplcNameChange

The name of the playlist has changed.

### -field wmplcMorph

Not supported.

### -field wmplcSort

The playlist has been sorted.

### -field wmplcLast

Last enumerated value. Not a valid change type.

## -see-also

<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>
