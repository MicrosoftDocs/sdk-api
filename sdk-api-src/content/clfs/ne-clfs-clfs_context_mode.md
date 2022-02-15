---
UID: NE:clfs._CLFS_CONTEXT_MODE
title: CLFS_CONTEXT_MODE (clfs.h)
description: Specifies a context mode type that indicates the direction and access methods that a client uses to scan a log.
helpviewer_keywords: ["*PCLFS_CONTEXT_MODE","CLFS_CONTEXT_MODE","CLFS_CONTEXT_MODE enumeration [Files]","ClfsContextForward","ClfsContextNone","ClfsContextPrevious","ClfsContextUndoNext","PCLFS_CONTEXT_MODE","PCLFS_CONTEXT_MODE enumeration pointer [Files]","PPCLFS_CONTEXT_MODE","PPCLFS_CONTEXT_MODE enumeration pointer [Files]","clfs/CLFS_CONTEXT_MODE","clfs/ClfsContextForward","clfs/ClfsContextNone","clfs/ClfsContextPrevious","clfs/ClfsContextUndoNext","clfs/PCLFS_CONTEXT_MODE","clfs/PPCLFS_CONTEXT_MODE","fs.clfs_context_mode"]
old-location: fs\clfs_context_mode.htm
tech.root: fs
ms.assetid: d71c18c3-42d5-4606-9915-8ea491e8b78f
ms.date: 12/05/2018
ms.keywords: '*PCLFS_CONTEXT_MODE, CLFS_CONTEXT_MODE, CLFS_CONTEXT_MODE enumeration [Files], ClfsContextForward, ClfsContextNone, ClfsContextPrevious, ClfsContextUndoNext, PCLFS_CONTEXT_MODE, PCLFS_CONTEXT_MODE enumeration pointer [Files], PPCLFS_CONTEXT_MODE, PPCLFS_CONTEXT_MODE enumeration pointer [Files], clfs/CLFS_CONTEXT_MODE, clfs/ClfsContextForward, clfs/ClfsContextNone, clfs/ClfsContextPrevious, clfs/ClfsContextUndoNext, clfs/PCLFS_CONTEXT_MODE, clfs/PPCLFS_CONTEXT_MODE, fs.clfs_context_mode'
req.header: clfs.h
req.include-header: Clfsw32.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: CLFS_CONTEXT_MODE, *PCLFS_CONTEXT_MODE, PPCLFS_CONTEXT_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLFS_CONTEXT_MODE
 - clfs/_CLFS_CONTEXT_MODE
 - PCLFS_CONTEXT_MODE
 - clfs/PCLFS_CONTEXT_MODE
 - CLFS_CONTEXT_MODE
 - clfs/CLFS_CONTEXT_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Clfs.h
api_name:
 - CLFS_CONTEXT_MODE
---

# CLFS_CONTEXT_MODE enumeration


## -description

Specifies a context mode type that indicates the direction and access methods  that a client uses to scan a log.  The context mode is set by using <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrecord">ReadLogRecord</a>, and is embedded in the  read context that these two functions return.

## -enum-fields

### -field ClfsContextNone:0x00

Do not move the cursor.

### -field ClfsContextUndoNext

Move the cursor backward to the next undo record.

### -field ClfsContextPrevious

Move the cursor to the previous log record from the current read context.

### -field ClfsContextForward

Move the cursor to the next client log record from the current read context.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrecord">ReadLogRecord</a>
