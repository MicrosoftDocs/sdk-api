---
UID: NF:processthreadsapi.SetThreadPriority
title: SetThreadPriority function (processthreadsapi.h)
description: Sets the priority value for the specified thread. This value, together with the priority class of the thread's process, determines the thread's base priority level.
old-location: base\setthreadpriority.htm
tech.root: processthreadsapi
ms.assetid: e3992e19-b546-4b0b-aa6a-dd9a7e330bf3
ms.date: 12/05/2018
ms.keywords: SetThreadPriority, SetThreadPriority function, THREAD_MODE_BACKGROUND_BEGIN, THREAD_MODE_BACKGROUND_END, THREAD_PRIORITY_ABOVE_NORMAL, THREAD_PRIORITY_BELOW_NORMAL, THREAD_PRIORITY_HIGHEST, THREAD_PRIORITY_IDLE, THREAD_PRIORITY_LOWEST, THREAD_PRIORITY_NORMAL, THREAD_PRIORITY_TIME_CRITICAL, _win32_setthreadpriority, base.setthreadpriority, processthreadsapi/SetThreadPriority, winbase/SetThreadPriority
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
 - SetThreadPriority
 - processthreadsapi/SetThreadPriority
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
 - SetThreadPriority
---

# SetThreadPriority function


## -description

Sets the priority value for the specified thread. This value, together with the priority class of the thread's process, determines the thread's base priority level.

## -parameters

### -param hThread [in]

A handle to the thread whose priority value is to be set.

The handle must have the <b>THREAD_SET_INFORMATION</b> or <b>THREAD_SET_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.<b>Windows Server 2003:  </b>The handle must have the <b>THREAD_SET_INFORMATION</b> access right.

### -param nPriority [in]

The priority value for the thread. This parameter can be one of the following values.

<table>
<tr>
<th>Priority</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="THREAD_MODE_BACKGROUND_BEGIN"></a><a id="thread_mode_background_begin"></a><dl>
<dt><b>THREAD_MODE_BACKGROUND_BEGIN</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Begin background processing mode. The system lowers the resource scheduling priorities of the thread so that it can perform background work without significantly affecting activity in the foreground.

This value can be specified only if <i>hThread</i> is a handle to the current thread.  The function fails if the thread is already in background processing mode.

<b>Windows Server 2003:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="THREAD_MODE_BACKGROUND_END"></a><a id="thread_mode_background_end"></a><dl>
<dt><b>THREAD_MODE_BACKGROUND_END</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
End background processing mode. The system restores the resource scheduling priorities of the thread as they were before the thread entered background processing mode.

This value can be specified only if <i>hThread</i> is a handle to the current thread. The function fails if the thread is not in background processing mode.

<b>Windows Server 2003:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="THREAD_PRIORITY_ABOVE_NORMAL"></a><a id="thread_priority_above_normal"></a><dl>
<dt><b>THREAD_PRIORITY_ABOVE_NORMAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Priority 1 point above the priority class.

</td>
</tr>
<tr>
<td width="40%"><a id="THREAD_PRIORITY_BELOW_NORMAL"></a><a id="thread_priority_below_normal"></a><dl>
<dt><b>THREAD_PRIORITY_BELOW_NORMAL</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
Priority 1 point below the priority class.

</td>
</tr>
<tr>
<td width="40%"><a id="THREAD_PRIORITY_HIGHEST"></a><a id="thread_priority_highest"></a><dl>
<dt><b>THREAD_PRIORITY_HIGHEST</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Priority 2 points above the priority class.

</td>
</tr>
<tr>
<td width="40%"><a id="THREAD_PRIORITY_IDLE"></a><a id="thread_priority_idle"></a><dl>
<dt><b>THREAD_PRIORITY_IDLE</b></dt>
<dt>-15</dt>
</dl>
</td>
<td width="60%">
Base priority of 1 for <b>IDLE_PRIORITY_CLASS</b>, <b>BELOW_NORMAL_PRIORITY_CLASS</b>, <b>NORMAL_PRIORITY_CLASS</b>, <b>ABOVE_NORMAL_PRIORITY_CLASS</b>, or <b>HIGH_PRIORITY_CLASS</b> processes, and a base priority of 16 for <b>REALTIME_PRIORITY_CLASS</b> processes.

</td>
</tr>
<tr>
<td width="40%"><a id="THREAD_PRIORITY_LOWEST"></a><a id="thread_priority_lowest"></a><dl>
<dt><b>THREAD_PRIORITY_LOWEST</b></dt>
<dt>-2</dt>
</dl>
</td>
<td width="60%">
Priority 2 points below the priority class.

</td>
</tr>
<tr>
<td width="40%"><a id="THREAD_PRIORITY_NORMAL"></a><a id="thread_priority_normal"></a><dl>
<dt><b>THREAD_PRIORITY_NORMAL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Normal priority for the priority class.

</td>
</tr>
<tr>
<td width="40%"><a id="THREAD_PRIORITY_TIME_CRITICAL"></a><a id="thread_priority_time_critical"></a><dl>
<dt><b>THREAD_PRIORITY_TIME_CRITICAL</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
Base priority of 15 for <b>IDLE_PRIORITY_CLASS</b>, <b>BELOW_NORMAL_PRIORITY_CLASS</b>, <b>NORMAL_PRIORITY_CLASS</b>, <b>ABOVE_NORMAL_PRIORITY_CLASS</b>, or <b>HIGH_PRIORITY_CLASS</b> processes, and a base priority of 31 for <b>REALTIME_PRIORITY_CLASS</b> processes.

</td>
</tr>
</table>
 

If the thread has the <b>REALTIME_PRIORITY_CLASS</b> base class, this parameter can also be -7, -6, -5, -4, -3, 3, 4, 5, or 6. For more information, see 
<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<b>Windows Phone 8.1:  </b>Windows Phone Store apps may call this function but it has no effect. The function will return a nonzero value indicating success.

## -remarks

Every thread has a base priority level determined by the thread's priority value and the priority class of its process. The system uses the base priority level of all executable threads to determine which thread gets the next slice of CPU time. Threads are scheduled in a round-robin fashion at each priority level, and only when there are no executable threads at a higher level does scheduling of threads at a lower level take place.

The 
<b>SetThreadPriority</b> function enables setting the base priority level of a thread relative to the priority class of its process. For example, specifying <b>THREAD_PRIORITY_HIGHEST</b> in a call to 
<b>SetThreadPriority</b> for a thread of an <b>IDLE_PRIORITY_CLASS</b> process sets the thread's base priority level to 6. For a table that shows the base priority levels for each combination of priority class and thread priority value, see 
<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>.

For <b>IDLE_PRIORITY_CLASS</b>, <b>BELOW_NORMAL_PRIORITY_CLASS</b>, <b>NORMAL_PRIORITY_CLASS</b>, <b>ABOVE_NORMAL_PRIORITY_CLASS</b>, and <b>HIGH_PRIORITY_CLASS</b> processes, the system dynamically boosts a thread's base priority level when events occur that are important to the thread. <b>REALTIME_PRIORITY_CLASS</b> processes do not receive dynamic boosts.

All threads initially start at <b>THREAD_PRIORITY_NORMAL</b>. Use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getpriorityclass">GetPriorityClass</a> and 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass">SetPriorityClass</a> functions to get and set the priority class of a process. Use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadpriority">GetThreadPriority</a> function to get the priority value of a thread.

Use the priority class of a process to differentiate between applications that are time critical and those that have normal or below normal scheduling requirements. Use thread priority values to differentiate the relative priorities of the tasks of a process. For example, a thread that handles input for a window could have a higher priority level than a thread that performs intensive calculations for the CPU.

When manipulating priorities, be very careful to ensure that a high-priority thread does not consume all of the available CPU time. A thread with a base priority level above 11 interferes with the normal operation of the operating system. Using <b>REALTIME_PRIORITY_CLASS</b> may cause disk caches to not flush, cause the mouse to stop responding, and so on.

The <b>THREAD_PRIORITY_*</b> values affect the CPU scheduling priority of the thread. For threads that perform background work such as file I/O, network I/O, or data processing, it is not sufficient to adjust the CPU scheduling priority; even an idle CPU priority thread can easily interfere with system responsiveness when it uses the disk and memory. Threads that perform background work should use the <b>THREAD_MODE_BACKGROUND_BEGIN</b> and <b>THREAD_MODE_BACKGROUND_END</b> values to adjust their resource scheduling priorities; threads that interact with the user should not use <b>THREAD_MODE_BACKGROUND_BEGIN</b>.

When a thread is in background processing mode, it should minimize sharing resources such as critical sections, heaps, and handles with other threads in the process, otherwise priority inversions can occur. If there are threads executing at high priority, a thread in background processing mode may not be scheduled promptly, but it will never be starved.

<b>Windows Server 2008 and Windows Vista:  </b>While the system is starting, the <b>SetThreadPriority</b> function returns a success return value but does not change thread priority  for applications that are started from the system Startup folder or listed in the <b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>Windows</b>&#92;<b>CurrentVersion</b>&#92;<b>Run</b> registry key. These applications run at reduced priority for a short time (approximately 60 seconds) to make the system more responsive to user actions during startup. 

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps.

<b>Windows Phone 8.1:</b>Windows Phone Store apps may call this function but it has no effect.


#### Examples

The following example demonstrates the use of thread background mode.


```cpp
#include <windows.h>
#include <tchar.h>

int main( void )
{
   DWORD dwError, dwThreadPri;

   if(!SetThreadPriority(GetCurrentThread(), THREAD_MODE_BACKGROUND_BEGIN))
   {
      dwError = GetLastError();
      if( ERROR_THREAD_MODE_ALREADY_BACKGROUND == dwError)
         _tprintf(TEXT("Already in background mode\n"));
      else _tprintf(TEXT("Failed to enter background mode (%d)\n"), dwError);
      goto Cleanup;
   } 

   // Display thread priority

   dwThreadPri = GetThreadPriority(GetCurrentThread());

   _tprintf(TEXT("Current thread priority is 0x%x\n"), dwThreadPri);

   //
   // Perform background work
   //
   ;

   if(!SetThreadPriority(GetCurrentThread(), THREAD_MODE_BACKGROUND_END))
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

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getpriorityclass">GetPriorityClass</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadpriority">GetThreadPriority</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass">SetPriorityClass</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>
