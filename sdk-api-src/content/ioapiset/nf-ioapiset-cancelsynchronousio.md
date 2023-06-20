---
UID: NF:ioapiset.CancelSynchronousIo
title: CancelSynchronousIo function (ioapiset.h)
description: Marks pending synchronous I/O operations that are issued by the specified thread as canceled.
helpviewer_keywords: ["CancelSynchronousIo","CancelSynchronousIo function [Files]","fs.cancelsynchronousio_func","ioapiset/CancelSynchronousIo","winbase/CancelSynchronousIo"]
old-location: fs\cancelsynchronousio_func.htm
tech.root: fs
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
ms.date: 12/05/2018
ms.keywords: CancelSynchronousIo, CancelSynchronousIo function [Files], fs.cancelsynchronousio_func, ioapiset/CancelSynchronousIo, winbase/CancelSynchronousIo
req.header: ioapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - CancelSynchronousIo
 - ioapiset/CancelSynchronousIo
dev_langs:
 - c++
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
 - CancelSynchronousIo
---

# CancelSynchronousIo function


## -description

Marks pending synchronous I/O operations that are issued by the specified thread as 
    canceled.

## -parameters

### -param hThread [in]

A handle to the thread.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

If this function cannot find a request to cancel, the return value is 0 (zero), and 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_NOT_FOUND</b>.

## -remarks

The caller must have the 
    <a href="/windows/desktop/ProcThread/thread-security-and-access-rights">THREAD_TERMINATE</a> access right.

If there are any pending I/O operations in progress for the specified thread, the 
    <b>CancelSynchronousIo</b> function marks them for 
    cancellation. Most types of operations can be canceled immediately; other operations can continue toward 
    completion before they are actually canceled and the caller is notified. The 
    <b>CancelSynchronousIo</b> function does not wait for 
    all canceled operations to complete. For more information, see 
    <a href="https://learn.microsoft.com/en-us/windows/win32/fileio/canceling-pending-i-o-operations">Canceling Pending I/O Operations</a>.

The operation being canceled is completed with one of three statuses; you must check the completion status to 
    determine the completion state. The three statuses are:

<ul>
<li><b>The operation completed normally.</b> This can occur even if the operation was 
      canceled, because the cancel request might not have been submitted in time to cancel the operation.</li>
<li><b>The operation was canceled.</b> The 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns 
      <b>ERROR_OPERATION_ABORTED</b>.</li>
<li><b>The operation failed with another error.</b> The 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the relevant error 
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

<a href="/windows/desktop/FileIO/cancelio">CancelIo</a>



<a href="/windows/desktop/FileIO/cancelioex-func">CancelIoEx</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>
