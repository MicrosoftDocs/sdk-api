---
UID: NF:ioapiset.CancelIoEx
title: CancelIoEx function (ioapiset.h)
author: windows-sdk-content
description: Marks any outstanding I/O operations for the specified file handle. The function only cancels I/O operations in the current process, regardless of which thread created the I/O operation.
old-location: fs\cancelioex_func.htm
tech.root: FileIO
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CancelIoEx, CancelIoEx function [Files], fs.cancelioex_func, ioapiset/CancelIoEx, winbase/CancelIoEx
ms.topic: function
req.header: ioapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-io-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-io-l1-1-1.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
 - CancelIoEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CancelIoEx function


## -description


Marks any outstanding I/O operations for the specified file handle. The function only cancels I/O 
    operations in the current process, regardless of which thread created the I/O operation.


## -parameters




### -param hFile [in]

A handle to the file.


### -param lpOverlapped [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> data structure that 
       contains the data used for asynchronous  I/O.

If this parameter is <b>NULL</b>, all I/O requests for the <i>hFile</i> 
       parameter are canceled.

If this parameter is not <b>NULL</b>, only those specific I/O requests that were issued 
       for the file with the specified <i>lpOverlapped</i> overlapped structure are marked as 
       canceled, meaning that you can cancel one or more requests, while the 
       <a href="https://msdn.microsoft.com/b28162dc-0da8-41c6-9901-29381d2d72c4">CancelIo</a> function cancels all outstanding requests on a file 
       handle.


## -returns



If the function succeeds, the return value is nonzero. The cancel operation for all pending I/O operations 
       issued by the calling process for the specified file handle was successfully requested. The application must not 
       free or reuse the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure associated with 
       the canceled I/O operations until they have completed. The thread can use the 
       <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> function to determine when 
       the I/O operations themselves have been completed.

If the function fails, the return value is 0 (zero). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

If this function cannot find a request to cancel, the return value is 0 (zero), and 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
       <b>ERROR_NOT_FOUND</b>.




## -remarks



The <b>CancelIoEx</b> function allows you to cancel 
    requests in threads other than the calling thread. The 
    <a href="https://msdn.microsoft.com/b28162dc-0da8-41c6-9901-29381d2d72c4">CancelIo</a> function only cancels requests in the same thread that 
    called the <b>CancelIo</b> function. 
    <b>CancelIoEx</b> cancels only outstanding I/O on the handle, 
    it does not change the state of the handle; this means that you cannot rely on the state of the handle because you 
    cannot know whether the operation was completed successfully or canceled.

If there are any pending I/O operations in progress for the specified file handle, the 
    <b>CancelIoEx</b> function marks them for cancellation. Most 
    types of operations can be canceled immediately; other operations can continue toward completion before they are 
    actually canceled and the caller is notified. The 
    <b>CancelIoEx</b> function does not wait for all canceled 
    operations to complete.

If the file handle is associated with a completion port, an I/O completion packet is not queued to the port if 
    a synchronous operation is successfully canceled. For asynchronous operations still pending, the cancel operation 
    will queue an I/O completion packet.

The operation being canceled is completed with one of three statuses; you must check the completion status to 
    determine the completion state. The three statuses are:

<ul>
<li>The operation completed normally. This can occur even if the operation was canceled, because the cancel 
      request might not have been submitted in time to cancel the operation.</li>
<li>The operation was canceled. The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> 
      function returns <b>ERROR_OPERATION_ABORTED</b>.</li>
<li>The operation failed with another error. The 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns the relevant error 
      code.</li>
</ul>
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




<a href="https://msdn.microsoft.com/b28162dc-0da8-41c6-9901-29381d2d72c4">CancelIo</a>



<a href="https://msdn.microsoft.com/f362c8b2-2193-443e-bb69-78f8b4147117">CancelSynchronousIo</a>



<a href="https://msdn.microsoft.com/adfe6d05-f30b-40a1-b3b0-58e2593e7b25">Canceling Pending I/O Operations</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/ade51d98-cc9d-4b33-9c52-559a9cb14707">Synchronous and Asynchronous I/O</a>
 

 

