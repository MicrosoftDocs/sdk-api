---
UID: NF:txfw32.TxfLogCreateRangeReadContext
title: TxfLogCreateRangeReadContext
description: Creates a context that is required to read any replication records.
tech.root: fs
helpviewer_keywords: ["TxfLogCreateRangeReadContext"]
ms.date: 4/26/2019
ms.keywords: TxfLogCreateRangeReadContext
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: TxfW32.dll
req.header: txfw32.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: TxfW32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - TxfLogCreateRangeReadContext
 - txfw32/TxfLogCreateRangeReadContext
dev_langs:
 - c++
topic_type:
 - apiref
 - kbSyntax
api_type:
 - DllExport
api_location:
 - TxfW32.dll
api_name:
 - TxfLogCreateRangeReadContext
---

## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Creates a context that is required to read any replication records.  In order to recover resources, the context must later be closed by calling TxfLogDestroyReadContext. Since the resources are allocated by a user-mode process, if that routine is not called, the resources will be recovered automatically when the process hosting the DLL terminates.

## -parameters

### -param LogPath

Location of the RM's CLFS BLF.

### -param BeginningLsn

Start of LSN range to search. (inclusive)

### -param EndingLsn

End of LSN range to search. (inclusive)

### -param BeginningVirtualClock

Start of the virtual clock.

### -param EndingVirtualClock

End of the virtual clock.

### -param RecordTypeMask

A mask value indicating the type of records.

### -param TxfLogContext

The returned context object.

## -returns

Returns S_OK on success.

## -remarks

## -see-also
