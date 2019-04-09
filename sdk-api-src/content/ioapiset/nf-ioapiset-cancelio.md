---
UID: NF:ioapiset.CancelIo
title: CancelIo function (ioapiset.h)
author: windows-sdk-content
description: Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file.
old-location: fs\cancelio.htm
tech.root: FileIO
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CancelIo, CancelIo function [Files], _win32_cancelio, base.cancelio, fs.cancelio, ioapiset/CancelIo, winbase/CancelIo
ms.topic: function
req.header: ioapiset.h
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
 - API-MS-Win-Core-io-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
 - CancelIo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CancelIo function


## -description


Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file. The function does not cancel I/O operations that other threads issue for a file handle.

To cancel I/O operations from another thread, use the <a href="https://msdn.microsoft.com/a2ce13b8-7da6-4848-848d-901d9667c2e3">CancelIoEx</a> function.


## -parameters




### -param hFile [in]

A handle to the file. 

The function cancels all pending I/O operations for this file handle.


## -returns



If the function succeeds, the return value is nonzero. The cancel operation for all pending I/O operations issued by the calling thread for the specified file handle was successfully requested. The thread can use the <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> function to determine when the I/O operations themselves have been completed.

If the function fails, the return value is zero (0). To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



If there are any pending I/O operations in progress for the specified file handle, and they are issued by the calling thread, the <b>CancelIo</b> function cancels them. <b>CancelIo</b> cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.

The I/O operations must be issued as overlapped I/O. If they are not, the I/O operations do not  return to allow the thread to call the 
<b>CancelIo</b> function. Calling the 
<b>CancelIo</b> function with a file handle that is not opened with <b>FILE_FLAG_OVERLAPPED</b> does nothing.

All I/O operations that are canceled complete with the error <b>ERROR_OPERATION_ABORTED</b>, and all completion notifications for the I/O operations occur normally.

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




<a href="https://msdn.microsoft.com/a2ce13b8-7da6-4848-848d-901d9667c2e3">CancelIoEx</a>



<a href="https://msdn.microsoft.com/f362c8b2-2193-443e-bb69-78f8b4147117">CancelSynchronousIo</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/30931ed0-495c-4b50-964a-c507d4ebc2be">LockFileEx</a>



<a href="https://msdn.microsoft.com/14dfc93d-557e-43d0-be45-8414cfd92c29">ReadDirectoryChangesW</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>



<a href="https://msdn.microsoft.com/ade51d98-cc9d-4b33-9c52-559a9cb14707">Synchronous and Asynchronous I/O</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>



<a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a>
 

 

