---
UID: NF:processthreadsapi.GetPriorityClass
title: GetPriorityClass function (processthreadsapi.h)
description: Retrieves the priority class for the specified process. This value, together with the priority value of each thread of the process, determines each thread's base priority level.
helpviewer_keywords: ["GetPriorityClass","GetPriorityClass function","_win32_getpriorityclass","base.getpriorityclass","processthreadsapi/GetPriorityClass","winbase/GetPriorityClass"]
old-location: base\getpriorityclass.htm
tech.root: processthreadsapi
ms.assetid: 2a16b18f-8efa-43f0-9f7d-d38cc8a153d3
ms.date: 12/05/2018
ms.keywords: GetPriorityClass, GetPriorityClass function, _win32_getpriorityclass, base.getpriorityclass, processthreadsapi/GetPriorityClass, winbase/GetPriorityClass
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetPriorityClass
 - processthreadsapi/GetPriorityClass
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
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetPriorityClass
---

# GetPriorityClass function


## -description

Retrieves the priority class for the specified process. This value, together with the priority value of each thread of the process, determines each thread's base priority level.

## -parameters

### -param hProcess [in]

A handle to the process. 




The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.

## -returns

If the function succeeds, the return value is the priority class of the specified process.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The process's priority class is one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ABOVE_NORMAL_PRIORITY_CLASS</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Process that has priority above <b>NORMAL_PRIORITY_CLASS</b> but below <b>HIGH_PRIORITY_CLASS</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BELOW_NORMAL_PRIORITY_CLASS</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
 Process that has priority above <b>IDLE_PRIORITY_CLASS</b> but below <b>NORMAL_PRIORITY_CLASS</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HIGH_PRIORITY_CLASS</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Process that performs time-critical tasks that must be executed immediately for it to run correctly. The threads of a high-priority class process preempt the threads of normal or idle priority class processes. An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system. Use extreme care when using the high-priority class, because a high-priority class CPU-bound application can use nearly all available cycles.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDLE_PRIORITY_CLASS</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Process whose threads run only when the system is idle and are preempted by the threads of any process running in a higher priority class. An example is a screen saver. The idle priority class is inherited by child processes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NORMAL_PRIORITY_CLASS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Process with no special scheduling needs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REALTIME_PRIORITY_CLASS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Process that has the highest possible priority. The threads of a real-time priority class process preempt the threads of all other processes, including operating system processes performing important tasks. For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or cause the mouse to be unresponsive.

</td>
</tr>
</table>

## -remarks

Every thread has a base priority level determined by the thread's priority value and the priority class of its process. The operating system uses the base priority level of all executable threads to determine which thread gets the next slice of CPU time. Threads are scheduled in a round-robin fashion at each priority level, and only when there are no executable threads at a higher level will scheduling of threads at a lower level take place.

For a table that shows the base priority levels for each combination of priority class and thread priority value, see <a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>.

Priority class is maintained by the executive, so all processes have a priority class that can be queried. 


#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/taking-a-snapshot-and-viewing-processes">Taking a Snapshot and Viewing Processes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadpriority">GetThreadPriority</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass">SetPriorityClass</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority">SetThreadPriority</a>