---
UID: NE:shobjidl_core._SPACTION
title: SPACTION (shobjidl_core.h)
description: Describes an action being performed that requires progress to be shown to the user using an IActionProgress interface.
helpviewer_keywords: ["SPACTION","SPACTION enumeration [Windows Shell]","SPACTION_APPLYINGATTRIBS","SPACTION_CALCULATING","SPACTION_COPYING","SPACTION_COPY_MOVING","SPACTION_DELETING","SPACTION_DOWNLOADING","SPACTION_FORMATTING","SPACTION_MOVING","SPACTION_NONE","SPACTION_RECYCLING","SPACTION_RENAMING","SPACTION_SEARCHING_FILES","SPACTION_SEARCHING_INTERNET","SPACTION_UPLOADING","shell.SPACTION","shell_SPACTION","shobjidl_core/SPACTION","shobjidl_core/SPACTION_APPLYINGATTRIBS","shobjidl_core/SPACTION_CALCULATING","shobjidl_core/SPACTION_COPYING","shobjidl_core/SPACTION_COPY_MOVING","shobjidl_core/SPACTION_DELETING","shobjidl_core/SPACTION_DOWNLOADING","shobjidl_core/SPACTION_FORMATTING","shobjidl_core/SPACTION_MOVING","shobjidl_core/SPACTION_NONE","shobjidl_core/SPACTION_RECYCLING","shobjidl_core/SPACTION_RENAMING","shobjidl_core/SPACTION_SEARCHING_FILES","shobjidl_core/SPACTION_SEARCHING_INTERNET","shobjidl_core/SPACTION_UPLOADING"]
old-location: shell\SPACTION.htm
tech.root: shell
ms.assetid: fc5a0f96-e8c2-483f-86b0-d8c870a9f77a
ms.date: 12/05/2018
ms.keywords: SPACTION, SPACTION enumeration [Windows Shell], SPACTION_APPLYINGATTRIBS, SPACTION_CALCULATING, SPACTION_COPYING, SPACTION_COPY_MOVING, SPACTION_DELETING, SPACTION_DOWNLOADING, SPACTION_FORMATTING, SPACTION_MOVING, SPACTION_NONE, SPACTION_RECYCLING, SPACTION_RENAMING, SPACTION_SEARCHING_FILES, SPACTION_SEARCHING_INTERNET, SPACTION_UPLOADING, shell.SPACTION, shell_SPACTION, shobjidl_core/SPACTION, shobjidl_core/SPACTION_APPLYINGATTRIBS, shobjidl_core/SPACTION_CALCULATING, shobjidl_core/SPACTION_COPYING, shobjidl_core/SPACTION_COPY_MOVING, shobjidl_core/SPACTION_DELETING, shobjidl_core/SPACTION_DOWNLOADING, shobjidl_core/SPACTION_FORMATTING, shobjidl_core/SPACTION_MOVING, shobjidl_core/SPACTION_NONE, shobjidl_core/SPACTION_RECYCLING, shobjidl_core/SPACTION_RENAMING, shobjidl_core/SPACTION_SEARCHING_FILES, shobjidl_core/SPACTION_SEARCHING_INTERNET, shobjidl_core/SPACTION_UPLOADING
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SPACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SPACTION
 - shobjidl_core/_SPACTION
 - SPACTION
 - shobjidl_core/SPACTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SPACTION
---

# SPACTION enumeration


## -description

Describes an action being performed that requires progress to be shown to the user using an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress">IActionProgress</a> interface.

## -enum-fields

### -field SPACTION_NONE:0

No action is being performed.

### -field SPACTION_MOVING

Files are being moved.

### -field SPACTION_COPYING

Files are being copied.

### -field SPACTION_RECYCLING

Files are being deleted.

### -field SPACTION_APPLYINGATTRIBS

A set of attributes are being applied to files.

### -field SPACTION_DOWNLOADING

A file is being downloaded from a remote source.

### -field SPACTION_SEARCHING_INTERNET

An Internet search is being performed.

### -field SPACTION_CALCULATING

A calculation is being performed.

### -field SPACTION_UPLOADING

A file is being uploaded to a remote source.

### -field SPACTION_SEARCHING_FILES

A local search is being performed.

### -field SPACTION_DELETING

<b>Windows Vista and later</b>. A deletion is being performed.

### -field SPACTION_RENAMING

<b>Windows Vista and later</b>. A renaming action is being performed.

### -field SPACTION_FORMATTING

<b>Windows Vista and later</b>. A formatting action is being performed.

### -field SPACTION_COPY_MOVING

<b>Windows 7 and later</b>. A copy or move action is being performed.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress">IActionProgress</a>
