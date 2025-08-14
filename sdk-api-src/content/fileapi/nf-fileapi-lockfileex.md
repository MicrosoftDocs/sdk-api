---
UID: NF:fileapi.LockFileEx
title: LockFileEx function (fileapi.h)
description: Locks the specified file for exclusive access by the calling process. This function can operate either synchronously or asynchronously and can request either an exclusive or a shared lock.
helpviewer_keywords: ["LOCKFILE_EXCLUSIVE_LOCK","LOCKFILE_FAIL_IMMEDIATELY","LockFileEx","LockFileEx function [Files]","_win32_lockfileex","base.lockfileex","fileapi/LockFileEx","fs.lockfileex","winbase/LockFileEx"]
old-location: fs\lockfileex.htm
tech.root: fs
ms.assetid: 30931ed0-495c-4b50-964a-c507d4ebc2be
ms.date: 12/05/2018
ms.keywords: LOCKFILE_EXCLUSIVE_LOCK, LOCKFILE_FAIL_IMMEDIATELY, LockFileEx, LockFileEx function [Files], _win32_lockfileex, base.lockfileex, fileapi/LockFileEx, fs.lockfileex, winbase/LockFileEx
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
 - LockFileEx
 - fileapi/LockFileEx
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
 - LockFileEx
---

# LockFileEx function


## -description

Locks the specified file  for exclusive access  by the calling process. This function can operate either synchronously or asynchronously and can request either an exclusive or a shared lock.

## -parameters

### -param hFile [in]

A handle to the file. The handle must have been created with either the <b>GENERIC_READ</b> or <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param dwFlags [in]

This parameter may be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOCKFILE_EXCLUSIVE_LOCK"></a><a id="lockfile_exclusive_lock"></a><dl>
<dt><b>LOCKFILE_EXCLUSIVE_LOCK</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The function requests an exclusive lock. Otherwise, it requests a shared lock.

</td>
</tr>
<tr>
<td width="40%"><a id="LOCKFILE_FAIL_IMMEDIATELY"></a><a id="lockfile_fail_immediately"></a><dl>
<dt><b>LOCKFILE_FAIL_IMMEDIATELY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The function returns immediately if it is unable to acquire the requested lock. Otherwise, it waits.

</td>
</tr>
</table>

### -param dwReserved

Reserved parameter; must be set to zero.

### -param nNumberOfBytesToLockLow [in]

The low-order 32 bits of the length of the byte range to lock.

### -param nNumberOfBytesToLockHigh [in]

The high-order 32 bits of the length of the byte range to lock.

### -param lpOverlapped [in, out]

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that the function uses with the locking request. This structure, which is required, contains the file offset of the beginning of the lock range. You must initialize the <b>hEvent</b> member to a valid handle or zero.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Locking a region of a file is used to acquire shared or exclusive access to the specified region using this file handle. If the file handle is  inherited by a process created by the locking process, the child process is not granted access to the locked region. If the locking process opens the file a second time, it cannot access the specified region through this second handle until it unlocks the region.

Locking a portion of a file for exclusive access denies all other processes both read and write access to the specified region of the file. Locking a region that goes beyond the current end-of-file position is not an error.

Locking a portion of a file for shared access denies all processes write access to the specified region of the file, including the process that first locks the region. All processes can read the locked region.

Locking a region of a file does not prevent reading or writing from a mapped file view.

The 
<b>LockFileEx</b> function operates asynchronously if the file handle was opened for asynchronous I/O, unless the <b>LOCKFILE_FAIL_IMMEDIATELY</b> flag is specified. If an exclusive lock is requested for a range of a file that already has a shared or exclusive lock, the function returns the error <b>ERROR_IO_PENDING</b>. The system will signal the event specified in the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure after the lock is granted. To determine when the lock has been granted, use the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function or one of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>. For more information, see <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

If the file handle was not opened for asynchronous I/O and the lock is not available, this call waits until the lock is granted or an error occurs, unless the <b>LOCKFILE_FAIL_IMMEDIATELY</b> flag is specified.

Exclusive locks cannot overlap an existing locked region of a file. Shared locks can overlap a locked region provided locks held on that region are shared locks. A shared lock can overlap an exclusive lock if both locks were created using the same file handle. When a shared lock overlaps an exclusive lock, the only possible access is a read by the owner of the locks. 
If the same range is locked with an exclusive and a shared lock, two unlock operations are necessary to unlock the region; the first unlock operation unlocks the exclusive lock, the second unlock operation unlocks the shared lock.


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



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-unlockfile">UnlockFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-unlockfileex">UnlockFileEx</a>