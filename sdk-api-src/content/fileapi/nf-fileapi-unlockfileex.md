---
UID: NF:fileapi.UnlockFileEx
title: UnlockFileEx function (fileapi.h)
description: Unlocks a region in the specified file. This function can operate either synchronously or asynchronously.
helpviewer_keywords: ["UnlockFileEx","UnlockFileEx function [Files]","_win32_unlockfileex","base.unlockfileex","fileapi/UnlockFileEx","fs.unlockfileex","winbase/UnlockFileEx"]
old-location: fs\unlockfileex.htm
tech.root: fs
ms.assetid: 78e2a75e-ff67-4039-b609-fb5004718c45
ms.date: 12/05/2018
ms.keywords: UnlockFileEx, UnlockFileEx function [Files], _win32_unlockfileex, base.unlockfileex, fileapi/UnlockFileEx, fs.unlockfileex, winbase/UnlockFileEx
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
 - UnlockFileEx
 - fileapi/UnlockFileEx
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
 - UnlockFileEx
---

# UnlockFileEx function


## -description

Unlocks a region in the specified file. This function can operate either synchronously or 
    asynchronously.

## -parameters

### -param hFile [in]

A handle to the file. The handle must have been created with either the 
      <b>GENERIC_READ</b> or <b>GENERIC_WRITE</b> access right. For more 
      information, see 
      <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param dwReserved

Reserved parameter; must be zero.

### -param nNumberOfBytesToUnlockLow [in]

The low-order part of the length of the byte range to unlock.

### -param nNumberOfBytesToUnlockHigh [in]

The high-order part of the length of the byte range to unlock.

### -param lpOverlapped [in, out]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that the 
      function uses with the unlocking request. This structure contains the file offset of the beginning of the unlock 
      range. You must initialize the <b>hEvent</b> member to a valid handle or zero. For more 
      information, see 
      <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero or <b>NULL</b>. To get extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Unlocking a region of a file releases a previously acquired lock on the file. The region to unlock must 
    correspond exactly to an existing locked region. Two adjacent regions of a file cannot be locked separately and 
    then unlocked using a single region that spans both locked regions.

Locks are released before the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function is 
    finished processing.

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



<a href="/windows/desktop/api/fileapi/nf-fileapi-lockfileex">LockFileEx</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-unlockfile">UnlockFile</a>