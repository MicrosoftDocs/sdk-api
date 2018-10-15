---
UID: NF:fileapi.UnlockFileEx
title: UnlockFileEx function
author: windows-sdk-content
description: Unlocks a region in the specified file. This function can operate either synchronously or asynchronously.
old-location: fs\unlockfileex.htm
tech.root: FileIO
ms.assetid: 78e2a75e-ff67-4039-b609-fb5004718c45
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: UnlockFileEx, UnlockFileEx function [Files], _win32_unlockfileex, base.unlockfileex, fileapi/UnlockFileEx, fs.unlockfileex, winbase/UnlockFileEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - UnlockFileEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
      <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -param dwReserved

Reserved parameter; must be zero.


### -param nNumberOfBytesToUnlockLow [in]

The low-order part of the length of the byte range to unlock.


### -param nNumberOfBytesToUnlockHigh [in]

The high-order part of the length of the byte range to unlock.


### -param lpOverlapped [in, out]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that the 
      function uses with the unlocking request. This structure contains the file offset of the beginning of the unlock 
      range. You must initialize the <b>hEvent</b> member to a valid handle or zero. For more 
      information, see 
      <a href="https://msdn.microsoft.com/ade51d98-cc9d-4b33-9c52-559a9cb14707">Synchronous and Asynchronous I/O</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero or <b>NULL</b>. To get extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Unlocking a region of a file releases a previously acquired lock on the file. The region to unlock must 
    correspond exactly to an existing locked region. Two adjacent regions of a file cannot be locked separately and 
    then unlocked using a single region that spans both locked regions.

Locks are released before the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function is 
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




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/c88e7b6c-c339-443b-adf9-0325807203dc">LockFile</a>



<a href="https://msdn.microsoft.com/30931ed0-495c-4b50-964a-c507d4ebc2be">LockFileEx</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/ade51d98-cc9d-4b33-9c52-559a9cb14707">Synchronous and Asynchronous I/O</a>



<a href="https://msdn.microsoft.com/6a930f83-3918-4688-ac60-d1de6857f479">UnlockFile</a>
 

 

