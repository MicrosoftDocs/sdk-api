---
UID: NE:clfs._CLFS_CONTEXT_MODE
title: "_CLFS_CONTEXT_MODE"
author: windows-sdk-content
description: Specifies a context mode type that indicates the direction and access methods that a client uses to scan a log.
old-location: fs\clfs_context_mode.htm
tech.root: Clfs
ms.assetid: d71c18c3-42d5-4606-9915-8ea491e8b78f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCLFS_CONTEXT_MODE, CLFS_CONTEXT_MODE, CLFS_CONTEXT_MODE enumeration [Files], ClfsContextForward, ClfsContextNone, ClfsContextPrevious, ClfsContextUndoNext, PCLFS_CONTEXT_MODE, PCLFS_CONTEXT_MODE enumeration pointer [Files], PPCLFS_CONTEXT_MODE, PPCLFS_CONTEXT_MODE enumeration pointer [Files], _CLFS_CONTEXT_MODE, clfs/CLFS_CONTEXT_MODE, clfs/ClfsContextForward, clfs/ClfsContextNone, clfs/ClfsContextPrevious, clfs/ClfsContextUndoNext, clfs/PCLFS_CONTEXT_MODE, clfs/PPCLFS_CONTEXT_MODE, fs.clfs_context_mode"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Clfs.h
api_name:
 - CLFS_CONTEXT_MODE
product: Windows
targetos: Windows
req.typenames: CLFS_CONTEXT_MODE, *PCLFS_CONTEXT_MODE, PPCLFS_CONTEXT_MODE
req.redist: 
---

# _CLFS_CONTEXT_MODE enumeration


## -description


Specifies a context mode type that indicates the direction and access methods  that a client uses to scan a log.  The context mode is set by using <a href="https://msdn.microsoft.com/1c56c47b-d898-4c70-ba70-8978057c66b9">ReadLogRecord</a>, and is embedded in the  read context that these two functions return.


## -enum-fields




### -field ClfsContextNone

Do not move the cursor.


### -field ClfsContextUndoNext

Move the cursor backward to the next undo record.


### -field ClfsContextPrevious

Move the cursor to the previous log record from the current read context.


### -field ClfsContextForward

Move the cursor to the next client log record from the current read context.


## -see-also




<a href="https://msdn.microsoft.com/1c56c47b-d898-4c70-ba70-8978057c66b9">ReadLogRecord</a>
 

 

