---
UID: NF:winbase.BackupSeek
title: BackupSeek function (winbase.h)
description: Seeks forward in a data stream initially accessed by using the BackupRead or BackupWrite function.
helpviewer_keywords: ["BackupSeek","BackupSeek function [Backup]","_win32_backupseek","backup.backupseek","base.backupseek","winbase/BackupSeek"]
old-location: backup\backupseek.htm
tech.root: Backup
ms.assetid: d5ffba3d-f744-49b4-83e0-e32bd45ecc4c
ms.date: 12/05/2018
ms.keywords: BackupSeek, BackupSeek function [Backup], _win32_backupseek, backup.backupseek, base.backupseek, winbase/BackupSeek
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BackupSeek
 - winbase/BackupSeek
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - api-ms-win-core-kernel32-legacy-l1-1-5.dll
 - api-ms-win-core-kernel32-legacy-l1-1-4.dll
 - api-ms-win-core-kernel32-legacy-l1-1-3.dll
 - api-ms-win-core-kernel32-legacy-l1-1-2.dll
 - api-ms-win-core-kernel32-legacy-l1-1-1.dll
 - api-ms-win-core-kernel32-legacy-l1-1-0.dll
 - Kernel32.dll
api_name:
 - BackupSeek
---

# BackupSeek function


## -description

The 
<b>BackupSeek</b> function seeks forward in a data stream initially accessed by using the 
<a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a> function.

## -parameters

### -param hFile [in]

Handle to the file or directory. This handle is created by using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

The handle must be synchronous (nonoverlapped). This means that the FILE_FLAG_OVERLAPPED flag must not be set when <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> is called. This function does not validate that the handle it receives is synchronous, so it does not return an error code for a synchronous handle, but calling it with an asynchronous (overlapped) handle can result in subtle errors that are very difficult to debug.

### -param dwLowBytesToSeek [in]

Low-order part of the number of bytes to seek.

### -param dwHighBytesToSeek [in]

High-order part of the number of bytes to seek.

### -param lpdwLowByteSeeked [out]

Pointer to a variable that receives the low-order bits of the number of bytes the function actually seeks.

### -param lpdwHighByteSeeked [out]

Pointer to a variable that receives the high-order bits of the number of bytes the function actually seeks.

### -param lpContext [in]

Pointer to an internal data structure used by the function. This structure must be the same structure that was initialized by the 
<a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a> or <a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a> function. An application must not touch the contents of this structure.

## -returns

If the function could seek the requested amount, the function returns a nonzero value.

If the function could not seek the requested amount, the function returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Applications use the <b>BackupSeek</b> function to skip portions of a data stream that cause errors. This function does not seek across stream headers. For example, this function cannot be used to skip the stream name. If an application attempts to seek past the end of a substream, the function fails, the <i>lpdwLowByteSeeked</i> and <i>lpdwHighByteSeeked</i> parameters indicate the actual number of bytes the function seeks, and the file position is placed at the start of the next stream header.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a>



<a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>