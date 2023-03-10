---
UID: NE:projectedfslib.PRJ_FILE_STATE
title: PRJ_FILE_STATE (projectedfslib.h)
description: The state of an item.
helpviewer_keywords: ["PRJ_FILE_STATE","PRJ_FILE_STATE enumeration","PRJ_FILE_STATE_DIRTY_PLACEHOLDER","PRJ_FILE_STATE_FULL","PRJ_FILE_STATE_HYDRATED_PLACEHOLDER","PRJ_FILE_STATE_PLACEHOLDER","PRJ_FILE_STATE_TOMBSTONE","ProjFS.prj_file_state","projectedfslib/PRJ_FILE_STATE","projectedfslib/PRJ_FILE_STATE_DIRTY_PLACEHOLDER","projectedfslib/PRJ_FILE_STATE_FULL","projectedfslib/PRJ_FILE_STATE_HYDRATED_PLACEHOLDER","projectedfslib/PRJ_FILE_STATE_PLACEHOLDER","projectedfslib/PRJ_FILE_STATE_TOMBSTONE"]
old-location: projfs\prj_file_state.htm
tech.root: ProjFS
ms.assetid: 9474C21B-47D4-468F-A970-0B0CBCF357A3
ms.date: 12/05/2018
ms.keywords: PRJ_FILE_STATE, PRJ_FILE_STATE enumeration, PRJ_FILE_STATE_DIRTY_PLACEHOLDER, PRJ_FILE_STATE_FULL, PRJ_FILE_STATE_HYDRATED_PLACEHOLDER, PRJ_FILE_STATE_PLACEHOLDER, PRJ_FILE_STATE_TOMBSTONE, ProjFS.prj_file_state, projectedfslib/PRJ_FILE_STATE, projectedfslib/PRJ_FILE_STATE_DIRTY_PLACEHOLDER, projectedfslib/PRJ_FILE_STATE_FULL, projectedfslib/PRJ_FILE_STATE_HYDRATED_PLACEHOLDER, projectedfslib/PRJ_FILE_STATE_PLACEHOLDER, projectedfslib/PRJ_FILE_STATE_TOMBSTONE
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
targetos: Windows
req.typenames: PRJ_FILE_STATE
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_FILE_STATE
 - projectedfslib/PRJ_FILE_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_FILE_STATE
---

# PRJ_FILE_STATE enumeration


## -description

The state of an item.

## -enum-fields

### -field PRJ_FILE_STATE_PLACEHOLDER:0x00000001

The item is a placeholder.

### -field PRJ_FILE_STATE_HYDRATED_PLACEHOLDER:0x00000002

The item is a hydrated placeholder, i.e., the item's content has been written to disk.

### -field PRJ_FILE_STATE_DIRTY_PLACEHOLDER:0x00000004

The placeholder item's metadata has been modified.

### -field PRJ_FILE_STATE_FULL:0x00000008

The item is full.

### -field PRJ_FILE_STATE_TOMBSTONE:0x00000010

The item is a tombstone.

## -remarks

The PRJ_FILE_STATE_FULL and PRJ_FILE_STATE_TOMBSTONE bits will not appear in combination with each other or any other bit.

