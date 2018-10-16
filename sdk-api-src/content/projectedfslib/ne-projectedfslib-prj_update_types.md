---
UID: NE:projectedfslib.PRJ_UPDATE_TYPES
title: PRJ_UPDATE_TYPES
author: windows-sdk-content
description: Flags to specify whether updates will be allowed given the state of a file or directory on disk.
old-location: projfs\prj_update_types.htm
tech.root: ProjFS
ms.assetid: E0E6F600-3B06-42D0-A87F-FAB4990562D0
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: PRJ_UPDATE_ALLOW_DIRTY_DATA, PRJ_UPDATE_ALLOW_DIRTY_METADATA, PRJ_UPDATE_ALLOW_READ_ONLY, PRJ_UPDATE_ALLOW_TOMBSTONE, PRJ_UPDATE_MAX_VAL, PRJ_UPDATE_NONE, PRJ_UPDATE_RESERVED1, PRJ_UPDATE_RESERVED2, PRJ_UPDATE_TYPES, PRJ_UPDATE_TYPES enumeration, ProjFS.prj_update_types, projectedfslib/PRJ_UPDATE_ALLOW_DIRTY_DATA, projectedfslib/PRJ_UPDATE_ALLOW_DIRTY_METADATA, projectedfslib/PRJ_UPDATE_ALLOW_READ_ONLY, projectedfslib/PRJ_UPDATE_ALLOW_TOMBSTONE, projectedfslib/PRJ_UPDATE_MAX_VAL, projectedfslib/PRJ_UPDATE_NONE, projectedfslib/PRJ_UPDATE_RESERVED1, projectedfslib/PRJ_UPDATE_RESERVED2, projectedfslib/PRJ_UPDATE_TYPES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - PRJ_UPDATE_TYPES
product: Windows
targetos: Windows
req.typenames: PRJ_UPDATE_TYPES
req.redist: 
---

# PRJ_UPDATE_TYPES enumeration


## -description


Flags to specify whether updates will be allowed given the state of a file or directory on disk.


## -enum-fields




### -field PRJ_UPDATE_NONE

Allow update only if the item is a placeholder (whether hydrated or not).


### -field PRJ_UPDATE_ALLOW_DIRTY_METADATA

Allow update if the item is a placeholder or a dirty placeholder.


### -field PRJ_UPDATE_ALLOW_DIRTY_DATA

Allow update if the item is a placeholder or if it is a full file.


### -field PRJ_UPDATE_ALLOW_TOMBSTONE

Allow update if the item is a placeholder or if it is a tombstone.


### -field PRJ_UPDATE_RESERVED1

Reserved for future use.


### -field PRJ_UPDATE_RESERVED2

Reserved for future use.


### -field PRJ_UPDATE_ALLOW_READ_ONLY

Allow update regardless of whether the DOS read-only bit is set on the item.


### -field PRJ_UPDATE_MAX_VAL

TBD


## -remarks







