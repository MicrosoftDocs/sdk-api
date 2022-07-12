---
UID: NF:winbase.ExecuteUmsThread
title: ExecuteUmsThread function (winbase.h)
description: Runs the specified UMS worker thread.
helpviewer_keywords: ["ExecuteUmsThread","ExecuteUmsThread function","base.executeumsthread","winbase/ExecuteUmsThread"]
old-location: base\executeumsthread.htm
tech.root: backup
ms.assetid: e4265351-e8e9-4878-bd42-93258b4cd1a0
ms.date: 12/05/2018
ms.keywords: ExecuteUmsThread, ExecuteUmsThread function, base.executeumsthread, winbase/ExecuteUmsThread
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - ExecuteUmsThread
 - winbase/ExecuteUmsThread
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - ExecuteUmsThread
req.apiset: api-ms-win-core-ums-l1-1-0 (introduced in Windows 7)
---

# ExecuteUmsThread function


## -description

Runs the specified UMS worker thread.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -parameters

### -param UmsThread [in, out]

A pointer to the UMS thread context of the worker thread to run.

## -returns

If the function succeeds, it does not return a value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RETRY</b></dt>
</dl>
</td>
<td width="60%">
The specified UMS worker thread is temporarily locked by the system. The caller can retry the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">UMS is not supported.</td>
</tr>
</table>

## -remarks

The <b>ExecuteUmsThread</b> function loads the state of the specified UMS worker thread over the state of the calling UMS scheduler thread so that the worker thread can run. The worker thread runs until it yields by calling the <a href="/windows/desktop/api/winbase/nf-winbase-umsthreadyield">UmsThreadYield</a> function, blocks, or terminates. 

When a worker thread yields or blocks, the system calls the scheduler thread's <a href="/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a> entry point function. When a previously blocked worker thread becomes unblocked, the system queues the worker thread to the completion list specified with the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute">UpdateProcThreadAttribute</a> function when the worker thread was created.

The <b>ExecuteUmsThread</b> function does not return unless an error occurs. If the function returns ERROR_RETRY, the error is transitory and the operation can be retried. 

If the function returns an error other than ERROR_RETRY, the application's scheduler should check whether the thread is suspended or terminated by calling <a href="/windows/desktop/api/winbase/nf-winbase-queryumsthreadinformation">QueryUmsThreadInformation</a> with <b>UmsThreadIsSuspended</b> or <b>UmsThreadIsTerminated</b>, respectively. Other possible errors include calling the function on a thread that is not   a UMS scheduler thread, passing an invalid UMS worker thread context, or specifying a worker thread that is already executing on another scheduler thread.

## -see-also

<a href="/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-umsthreadyield">UmsThreadYield</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute">UpdateProcThreadAttribute</a>
