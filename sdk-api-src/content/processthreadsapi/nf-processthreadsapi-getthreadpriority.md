---
UID: NF:processthreadsapi.GetThreadPriority
title: GetThreadPriority function (processthreadsapi.h)
description: Retrieves the priority value for the specified thread. This value, together with the priority class of the thread's process, determines the thread's base-priority level.
helpviewer_keywords: ["GetThreadPriority","GetThreadPriority function","_win32_getthreadpriority","base.getthreadpriority","processthreadsapi/GetThreadPriority","winbase/GetThreadPriority"]
old-location: base\getthreadpriority.htm
tech.root: processthreadsapi
ms.assetid: 9e5ce4e8-bdd1-48c3-aa1d-b24b2b7bfb00
ms.date: 12/05/2018
ms.keywords: GetThreadPriority, GetThreadPriority function, _win32_getthreadpriority, base.getthreadpriority, processthreadsapi/GetThreadPriority, winbase/GetThreadPriority
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: Kernel32.dll; KernelBase.dll on Windows Phone 8.1
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThreadPriority
 - processthreadsapi/GetThreadPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - KernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadPriority
---

# GetThreadPriority function


## -description

Retrieves the priority value for the specified thread. This value, together with the priority class of the thread's process, determines the thread's base-priority level.

## -parameters

### -param hThread [in]

A handle to the thread.

The handle must have the <b>THREAD_QUERY_INFORMATION</b> or <b>THREAD_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

<b>Windows Server 2003:  </b>The handle must have the <b>THREAD_QUERY_INFORMATION</b> access right.

## -returns

If the function succeeds, the return value is the thread's priority level.

If the function fails, the return value is <b>THREAD_PRIORITY_ERROR_RETURN</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<b>Windows Phone 8.1:  </b>This function will always return <b>THREAD_PRIORITY_NORMAL</b>.

The thread's priority level is one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>THREAD_PRIORITY_ABOVE_NORMAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Priority 1 point above the priority class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>THREAD_PRIORITY_BELOW_NORMAL</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
Priority 1 point below the priority class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>THREAD_PRIORITY_HIGHEST</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Priority 2 points above the priority class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>THREAD_PRIORITY_IDLE</b></dt>
<dt>-15</dt>
</dl>
</td>
<td width="60%">
Base priority of 1 for <b>IDLE_PRIORITY_CLASS</b>, <b>BELOW_NORMAL_PRIORITY_CLASS</b>, <b>NORMAL_PRIORITY_CLASS</b>, <b>ABOVE_NORMAL_PRIORITY_CLASS</b>, or <b>HIGH_PRIORITY_CLASS</b> processes, and a base priority of 16 for <b>REALTIME_PRIORITY_CLASS</b> processes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>THREAD_PRIORITY_LOWEST</b></dt>
<dt>-2</dt>
</dl>
</td>
<td width="60%">
Priority 2 points below the priority class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>THREAD_PRIORITY_NORMAL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Normal priority for the priority class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>THREAD_PRIORITY_TIME_CRITICAL</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
Base-priority level of 15 for <b>IDLE_PRIORITY_CLASS</b>, <b>BELOW_NORMAL_PRIORITY_CLASS</b>, <b>NORMAL_PRIORITY_CLASS</b>, <b>ABOVE_NORMAL_PRIORITY_CLASS</b>, or <b>HIGH_PRIORITY_CLASS</b> processes, and a base-priority level of 31 for <b>REALTIME_PRIORITY_CLASS</b> processes.

</td>
</tr>
</table>
 

If the thread has the <b>REALTIME_PRIORITY_CLASS</b> base class, this function can also return one of the following values: -7, -6, -5, -4, -3, 3, 4, 5, or 6. For more information, see 
<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>.

## -remarks

Every thread has a base-priority level determined by the thread's priority value and the priority class of its process. The operating system uses the base-priority level of all executable threads to determine which thread gets the next slice of CPU time. Threads are scheduled in a round-robin fashion at each priority level, and only when there are no executable threads at a higher level will scheduling of threads at a lower level take place.

For a table that shows the base-priority levels for each combination of priority class and thread priority value, refer to the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass">SetPriorityClass</a> function.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps.

<b>Windows Phone 8.1:</b>Windows Phone Store apps may call this function but it has no effect.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getpriorityclass">GetPriorityClass</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass">SetPriorityClass</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority">SetThreadPriority</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>