---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetPriorityClass function


## -description


Retrieves the priority class for the specified process. This value, together with the priority value of each thread of the process, determines each thread's base priority level.


## -parameters




### -param hProcess [in]

A handle to the process. 




The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.


## -returns



If the function succeeds, the return value is the priority class of the specified process.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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

For a table that shows the base priority levels for each combination of priority class and thread priority value, see <a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>.

Priority class is maintained by the executive, so all processes have a priority class that can be queried. 


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/318d166f-858f-4f33-9422-977e0c4beb3f">Taking a Snapshot and Viewing Processes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9e5ce4e8-bdd1-48c3-aa1d-b24b2b7bfb00">GetThreadPriority</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>



<a href="https://msdn.microsoft.com/02686637-427a-4cf1-a4e5-60c707af3084">SetPriorityClass</a>



<a href="https://msdn.microsoft.com/e3992e19-b546-4b0b-aa6a-dd9a7e330bf3">SetThreadPriority</a>
 

 

