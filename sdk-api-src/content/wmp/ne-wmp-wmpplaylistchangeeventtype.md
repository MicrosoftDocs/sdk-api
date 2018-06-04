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

# WMPPlaylistChangeEventType enumeration


## -description



The <b>WMPPlaylistChangeEventType</b> enumeration type defines the types of changes that can be made to a playlist.




## -enum-fields




### -field wmplcUnknown

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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

