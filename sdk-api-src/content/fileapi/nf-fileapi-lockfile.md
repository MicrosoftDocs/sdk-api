---
UID: NF:fileapi.LockFile
title: LockFile function
author: windows-sdk-content
description: Locks the specified file for exclusive access by the calling process.
old-location: fs\lockfile.htm
old-project: FileIO
ms.assetid: c88e7b6c-c339-443b-adf9-0325807203dc
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: LockFile, LockFile function [Files], _win32_lockfile, base.lockfile, fileapi/LockFile, fs.lockfile, winbase/LockFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAM_INFO_LEVELS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# LockFile function


## -description


Locks the specified file  for exclusive access  by the calling process.

To specify additional options, for example creating a shared lock or for block-on-fail operation, use the 
<a href="https://msdn.microsoft.com/30931ed0-495c-4b50-964a-c507d4ebc2be">LockFileEx</a> function.


## -parameters




### -param hFile [in]

A handle to the file. The file handle must have been created with the <b>GENERIC_READ</b> or <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the call to <b>LockFile</b> completes synchronously, a completion entry may not be queued when a completion port is associated with the file handle.

The 
<a href="https://msdn.microsoft.com/6a930f83-3918-4688-ac60-d1de6857f479">UnlockFile</a> function unlocks a file region locked by 
<b>LockFile</b>.

Locking a region of a file gives the threads of the locking process exclusive access to the specified region using this file handle. If the file handle is  inherited by a process created by the locking process, the child process is not granted access to the locked region. If the locking process opens the file a second time, it cannot access the specified region through this second handle until it unlocks the region.

Locking a region of a file does not prevent reading from a mapped file view.

You can lock bytes that are beyond the end of the current  file. This is useful to coordinate adding records to the end of a file.

Exclusive locks cannot overlap an existing locked region of a file. For more information, see <a href="https://msdn.microsoft.com/30931ed0-495c-4b50-964a-c507d4ebc2be">LockFileEx</a>.

If 
<b>LockFile</b> cannot lock a region of a file, it returns zero immediately. It does not block. To issue a file lock request that will block until the lock is acquired, use 
<a href="https://msdn.microsoft.com/30931ed0-495c-4b50-964a-c507d4ebc2be">LockFileEx</a> without the <b>LOCKFILE_FAIL_IMMEDIATELY</b> flag.

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
<a href="https://msdn.microsoft.com/e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5">Appending One File to Another File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/30931ed0-495c-4b50-964a-c507d4ebc2be">LockFileEx</a>



<a href="https://msdn.microsoft.com/6a930f83-3918-4688-ac60-d1de6857f479">UnlockFile</a>
 

 

