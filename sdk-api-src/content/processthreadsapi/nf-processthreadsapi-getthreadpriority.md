---
UID: NF:processthreadsapi.GetThreadPriority
title: GetThreadPriority function
author: windows-sdk-content
description: Retrieves the priority value for the specified thread. This value, together with the priority class of the thread's process, determines the thread's base-priority level.
old-location: base\getthreadpriority.htm
tech.root: procthread
ms.assetid: 9e5ce4e8-bdd1-48c3-aa1d-b24b2b7bfb00
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetThreadPriority, GetThreadPriority function, _win32_getthreadpriority, base.getthreadpriority, processthreadsapi/GetThreadPriority, winbase/GetThreadPriority
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThreadPriority function


## -description


Retrieves the priority value for the specified thread. This value, together with the priority class of the thread's process, determines the thread's base-priority level.


## -parameters




### -param hThread [in]

A handle to the thread.

The handle must have the <b>THREAD_QUERY_INFORMATION</b> or <b>THREAD_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.

<b>Windows Server 2003:  </b>The handle must have the <b>THREAD_QUERY_INFORMATION</b> access right.


## -returns



If the function succeeds, the return value is the thread's priority level.

If the function fails, the return value is <b>THREAD_PRIORITY_ERROR_RETURN</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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
<a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>.




## -remarks



Every thread has a base-priority level determined by the thread's priority value and the priority class of its process. The operating system uses the base-priority level of all executable threads to determine which thread gets the next slice of CPU time. Threads are scheduled in a round-robin fashion at each priority level, and only when there are no executable threads at a higher level will scheduling of threads at a lower level take place.

For a table that shows the base-priority levels for each combination of priority class and thread priority value, refer to the 
<a href="https://msdn.microsoft.com/02686637-427a-4cf1-a4e5-60c707af3084">SetPriorityClass</a> function.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps.

<b>Windows Phone 8.1:</b>Windows Phone Store apps may call this function but it has no effect.




## -see-also




<a href="https://msdn.microsoft.com/2a16b18f-8efa-43f0-9f7d-d38cc8a153d3">GetPriorityClass</a>



<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>



<a href="https://msdn.microsoft.com/02686637-427a-4cf1-a4e5-60c707af3084">SetPriorityClass</a>



<a href="https://msdn.microsoft.com/e3992e19-b546-4b0b-aa6a-dd9a7e330bf3">SetThreadPriority</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

