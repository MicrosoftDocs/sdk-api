---
UID: NF:fileapi.LockFile
title: LockFile function (fileapi.h)
description: Locks the specified file for exclusive access by the calling process.
helpviewer_keywords: ["LockFile","LockFile function [Files]","_win32_lockfile","base.lockfile","fileapi/LockFile","fs.lockfile","winbase/LockFile"]
old-location: fs\lockfile.htm
tech.root: fs
ms.assetid: c88e7b6c-c339-443b-adf9-0325807203dc
ms.date: 12/05/2018
ms.keywords: LockFile, LockFile function [Files], _win32_lockfile, base.lockfile, fileapi/LockFile, fs.lockfile, winbase/LockFile
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
 - LockFile
 - fileapi/LockFile
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
 - LockFile
---

# LockFile function


## -description

Locks the specified file  for exclusive access  by the calling process.

To specify additional options, for example creating a shared lock or for block-on-fail operation, use the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-lockfileex">LockFileEx</a> function.

## -parameters

### -param hFile [in]

A handle to the file. The file handle must have been created with the <b>GENERIC_READ</b> or <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param dwFileOffsetLow [in]

The low-order 32 bits of the starting byte offset in the file where the lock should begin.

### -param dwFileOffsetHigh [in]

The high-order 32 bits of the starting byte offset in the file where the lock should begin.

### -param nNumberOfBytesToLockLow [in]

The low-order 32 bits of the length of the byte range to be locked.

### -param nNumberOfBytesToLockHigh [in]

The high-order 32 bits of the length of the byte range to be locked.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the call to <b>LockFile</b> completes synchronously, a completion entry may not be queued when a completion port is associated with the file handle.

The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-unlockfile">UnlockFile</a> function unlocks a file region locked by 
<b>LockFile</b>.

Locking a region of a file gives the threads of the locking process exclusive access to the specified region using this file handle. If the file handle is  inherited by a process created by the locking process, the child process is not granted access to the locked region. If the locking process opens the file a second time, it cannot access the specified region through this second handle until it unlocks the region.

Locking a region of a file does not prevent reading or writing from a mapped file view.

You can lock bytes that are beyond the end of the current  file. This is useful to coordinate adding records to the end of a file.

Exclusive locks cannot overlap an existing locked region of a file. For more information, see <a href="/windows/desktop/api/fileapi/nf-fileapi-lockfileex">LockFileEx</a>.

If 
<b>LockFile</b> cannot lock a region of a file, it returns zero immediately. It does not block. To issue a file lock request that will block until the lock is acquired, use 
<a href="/windows/desktop/api/fileapi/nf-fileapi-lockfileex">LockFileEx</a> without the <b>LOCKFILE_FAIL_IMMEDIATELY</b> flag.

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
 


#### Examples

For an example, see 
<a href="/windows/desktop/FileIO/appending-one-file-to-another-file">Appending One File to Another File</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/FileIO/locking-and-unlocking-byte-ranges-in-files">Locking and Unlocking Byte Ranges in Files</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-lockfileex">LockFileEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-unlockfile">UnlockFile</a>