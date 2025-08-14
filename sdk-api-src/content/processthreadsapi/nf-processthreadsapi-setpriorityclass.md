---
UID: NF:processthreadsapi.SetPriorityClass
title: SetPriorityClass function (processthreadsapi.h)
description: Sets the priority class for the specified process. This value together with the priority value of each thread of the process determines each thread's base priority level.
helpviewer_keywords: ["ABOVE_NORMAL_PRIORITY_CLASS","BELOW_NORMAL_PRIORITY_CLASS","HIGH_PRIORITY_CLASS","IDLE_PRIORITY_CLASS","NORMAL_PRIORITY_CLASS","PROCESS_MODE_BACKGROUND_BEGIN","PROCESS_MODE_BACKGROUND_END","REALTIME_PRIORITY_CLASS","SetPriorityClass","SetPriorityClass function","_win32_setpriorityclass","base.setpriorityclass","processthreadsapi/SetPriorityClass","winbase/SetPriorityClass"]
old-location: base\setpriorityclass.htm
tech.root: processthreadsapi
ms.assetid: 02686637-427a-4cf1-a4e5-60c707af3084
ms.date: 12/05/2018
ms.keywords: ABOVE_NORMAL_PRIORITY_CLASS, BELOW_NORMAL_PRIORITY_CLASS, HIGH_PRIORITY_CLASS, IDLE_PRIORITY_CLASS, NORMAL_PRIORITY_CLASS, PROCESS_MODE_BACKGROUND_BEGIN, PROCESS_MODE_BACKGROUND_END, REALTIME_PRIORITY_CLASS, SetPriorityClass, SetPriorityClass function, _win32_setpriorityclass, base.setpriorityclass, processthreadsapi/SetPriorityClass, winbase/SetPriorityClass
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
 - SetPriorityClass
 - processthreadsapi/SetPriorityClass
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
 - SetPriorityClass
---

# SetPriorityClass function


## -description

Sets the priority class for the specified process. This value together with the priority value of each thread of the process determines each thread's base priority level.

## -parameters

### -param hProcess [in]

A handle to the process. 




The handle must have the <b>PROCESS_SET_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param dwPriorityClass [in]

The priority class for the process. This parameter can be one of the following values.

<table>
<tr>
<th>Priority</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ABOVE_NORMAL_PRIORITY_CLASS"></a><a id="above_normal_priority_class"></a><dl>
<dt><b>ABOVE_NORMAL_PRIORITY_CLASS</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
 Process that has priority above <b>NORMAL_PRIORITY_CLASS</b> but below <b>HIGH_PRIORITY_CLASS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="BELOW_NORMAL_PRIORITY_CLASS"></a><a id="below_normal_priority_class"></a><dl>
<dt><b>BELOW_NORMAL_PRIORITY_CLASS</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
 Process that has priority above <b>IDLE_PRIORITY_CLASS</b> but below <b>NORMAL_PRIORITY_CLASS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="HIGH_PRIORITY_CLASS"></a><a id="high_priority_class"></a><dl>
<dt><b>HIGH_PRIORITY_CLASS</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Process that performs time-critical tasks that must be executed immediately. The threads of the process preempt the threads of normal or idle priority class processes. An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system. Use extreme care when using the high-priority class, because a high-priority class application can use nearly all available CPU time.

</td>
</tr>
<tr>
<td width="40%"><a id="IDLE_PRIORITY_CLASS"></a><a id="idle_priority_class"></a><dl>
<dt><b>IDLE_PRIORITY_CLASS</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Process whose threads run only when the system is idle. The threads of the process are preempted by the threads of any process running in a higher priority class. An example is a screen saver. The idle-priority class is inherited by child processes.

</td>
</tr>
<tr>
<td width="40%"><a id="NORMAL_PRIORITY_CLASS"></a><a id="normal_priority_class"></a><dl>
<dt><b>NORMAL_PRIORITY_CLASS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Process with no special scheduling needs.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_MODE_BACKGROUND_BEGIN"></a><a id="process_mode_background_begin"></a><dl>
<dt><b>PROCESS_MODE_BACKGROUND_BEGIN</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Begin background processing mode. The system lowers the resource scheduling priorities of the process (and its threads) so that it can perform background work without significantly affecting activity in the foreground.

This value can be specified only if <i>hProcess</i> is a handle to the current process. The function fails if the process is already in background processing mode.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_MODE_BACKGROUND_END"></a><a id="process_mode_background_end"></a><dl>
<dt><b>PROCESS_MODE_BACKGROUND_END</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
End background processing mode. The system restores the resource scheduling priorities of the process (and its threads) as they were before the process entered background processing mode.

This value can be specified only if <i>hProcess</i> is a handle to the current process. The function fails if the process is not in background processing mode.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="REALTIME_PRIORITY_CLASS"></a><a id="realtime_priority_class"></a><dl>
<dt><b>REALTIME_PRIORITY_CLASS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Process that has the highest possible priority. The threads of the process preempt the threads of all other processes, including operating system processes performing important tasks. For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or cause the mouse to be unresponsive.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Every thread has a base priority level determined by the thread's priority value and the priority class of its process. The system uses the base priority level of all executable threads to determine which thread gets the next slice of CPU time. The 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority">SetThreadPriority</a> function enables setting the base priority level of a thread relative to the priority class of its process. For more information, see 
<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>.

The <b>*_PRIORITY_CLASS</b> values affect the CPU scheduling priority of the process. For processes that perform background work such as file I/O, network I/O, or data processing, it is not sufficient to adjust the CPU scheduling priority; even an idle CPU priority process can easily interfere with system responsiveness when it uses the disk and memory. Processes that perform background work should use the <b>PROCESS_MODE_BACKGROUND_BEGIN</b> and <b>PROCESS_MODE_BACKGROUND_END</b> values to adjust their resource scheduling priorities; processes that interact with the user should not use <b>PROCESS_MODE_BACKGROUND_BEGIN</b>.

If a process is in background processing mode, the new threads it creates will also be in background processing mode. When a thread is in background processing mode, it should minimize sharing resources such as critical sections, heaps, and handles with other threads in the process, otherwise priority inversions can occur. If there are threads executing at high priority, a thread in background processing mode may not be scheduled promptly, but it will never be starved.

Each  thread can enter background processing mode independently using <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority">SetThreadPriority</a>. Do not call <b>SetPriorityClass</b> to enter background processing mode after a thread in the process has called <b>SetThreadPriority</b> to enter background processing mode. After a process ends background processing mode, it resets all threads in the process; however, it is not possible for the process to know which threads were already in background processing mode.


#### Examples

The following example demonstrates the use of process background mode.


```cpp
#include <windows.h>
#include <tchar.h>

int main( void )
{
   DWORD dwError, dwPriClass;

   if(!SetPriorityClass(GetCurrentProcess(), PROCESS_MODE_BACKGROUND_BEGIN))
   {
      dwError = GetLastError();
      if( ERROR_PROCESS_MODE_ALREADY_BACKGROUND == dwError)
         _tprintf(TEXT("Already in background mode\n"));
      else _tprintf(TEXT("Failed to enter background mode (%d)\n"), dwError);
      goto Cleanup;
   } 

   // Display priority class

   dwPriClass = GetPriorityClass(GetCurrentProcess());

   _tprintf(TEXT("Current priority class is 0x%x\n"), dwPriClass);

   //
   // Perform background work
   //
   ;

   if(!SetPriorityClass(GetCurrentProcess(), PROCESS_MODE_BACKGROUND_END))
   {
      _tprintf(TEXT("Failed to end background mode (%d)\n"), GetLastError());
   }

Cleanup:
   // Clean up
   ;
return 0;
}

```

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getpriorityclass">GetPriorityClass</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadpriority">GetThreadPriority</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority">SetThreadPriority</a>