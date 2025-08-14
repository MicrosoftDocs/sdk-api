---
UID: NF:fileapi.UnlockFile
title: UnlockFile function (fileapi.h)
description: Unlocks a region in an open file.
helpviewer_keywords: ["UnlockFile","UnlockFile function [Files]","_win32_unlockfile","base.unlockfile","fileapi/UnlockFile","fs.unlockfile","winbase/UnlockFile"]
old-location: fs\unlockfile.htm
tech.root: fs
ms.assetid: 6a930f83-3918-4688-ac60-d1de6857f479
ms.date: 12/05/2018
ms.keywords: UnlockFile, UnlockFile function [Files], _win32_unlockfile, base.unlockfile, fileapi/UnlockFile, fs.unlockfile, winbase/UnlockFile
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - UnlockFile
 - fileapi/UnlockFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - UnlockFile
---

# UnlockFile function


## -description

Unlocks a region in an open file. Unlocking a region enables other processes to access the region.

For an alternate way to specify the region, use the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-unlockfileex">UnlockFileEx</a> function.

## -parameters

### -param hFile [in]

A handle to the file that contains a region locked with 
<a href="/windows/desktop/api/fileapi/nf-fileapi-lockfile">LockFile</a>. The file handle must have been created with either the <b>GENERIC_READ</b> or <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param dwFileOffsetLow [in]

The low-order word of the starting byte offset in the file where the locked region begins.

### -param dwFileOffsetHigh [in]

The high-order word of the starting byte offset in the file where the locked region begins.

### -param nNumberOfBytesToUnlockLow [in]

The low-order word of the length of the byte range to be unlocked.

### -param nNumberOfBytesToUnlockHigh [in]

The high-order word of the length of the byte range to be unlocked.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function always operates synchronously, but may not queue a completion entry when a completion port is associated with the file handle.

Unlocking a region of a file releases a previously acquired lock on the file. The region to unlock must correspond exactly to an existing locked region. Two adjacent regions of a file cannot be locked separately and then unlocked using a single region that spans both locked regions.

If a process terminates with a portion of a file locked or closes a file that has outstanding locks, the locks are unlocked by the operating system. However, the time it takes for the operating system to unlock these locks depends upon available system resources. Therefore, it is recommended that your process explicitly unlock all files it has locked when it terminates. If this is not done, access to these files may be denied if the operating system has not yet unlocked them.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/FileIO/locking-and-unlocking-byte-ranges-in-files">Locking and Unlocking Byte Ranges in Files</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-lockfile">LockFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-unlockfileex">UnlockFileEx</a>