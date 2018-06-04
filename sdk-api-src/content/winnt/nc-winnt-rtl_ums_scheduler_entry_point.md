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

# RTL_UMS_SCHEDULER_ENTRY_POINT callback function


## -description


The application-defined user-mode scheduling (UMS) scheduler entry point function associated with a UMS completion list. 

The <b>PUMS_SCHEDULER_ENTRY_POINT</b> type defines a pointer to this function. <i>UmsSchedulerProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param Reason [in]

The reason the scheduler entry point is being called. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UmsSchedulerStartup"></a><a id="umsschedulerstartup"></a><a id="UMSSCHEDULERSTARTUP"></a><dl>
<dt><b>UmsSchedulerStartup</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
A UMS scheduler thread was created. The entry point is called with this reason once each time  <a href="https://msdn.microsoft.com/792bd7fa-0ae9-4c38-a664-5fb3e3d0c52b">EnterUmsSchedulingMode</a> is called.

</td>
</tr>
<tr>
<td width="40%"><a id="UmsSchedulerThreadBlocked"></a><a id="umsschedulerthreadblocked"></a><a id="UMSSCHEDULERTHREADBLOCKED"></a><dl>
<dt><b>UmsSchedulerThreadBlocked</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A UMS worker thread blocked.

</td>
</tr>
<tr>
<td width="40%"><a id="UmsSchedulerThreadYield"></a><a id="umsschedulerthreadyield"></a><a id="UMSSCHEDULERTHREADYIELD"></a><dl>
<dt><b>UmsSchedulerThreadYield</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An executing UMS worker thread yielded control by calling the <a href="https://msdn.microsoft.com/d7c94ed5-9536-4c39-8658-27e4237cc9ba">UmsThreadYield</a> function. 

</td>
</tr>
</table>
 


### -param ActivationPayload [in]

If the <i>Reason</i> parameter is <b>UmsSchedulerStartup</b>, this parameter is NULL.

If the <i>Reason</i> parameter is  <b>UmsSchedulerThreadBlocked</b>, bit 0 of this parameter indicates the type of activity that was being serviced when the UMS worker thread blocked. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The thread blocked on a trap (for example, a hard page fault) or an interrupt (for example, an asynchronous procedure call).

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The thread blocked on a system call.

</td>
</tr>
</table>
 

If the <i>Reason</i> parameter is <b>UmsSchedulerThreadYield</b>, this parameter is a pointer to the UMS thread context of the UMS worker thread that yielded. 


### -param SchedulerParam [in]

If the <i>Reason</i> parameter is <b>UmsSchedulerStartup</b>, this parameter is the <b>SchedulerParam</b> member of the <a href="https://msdn.microsoft.com/e3f7b1b7-d2b8-432d-bce7-3633292e855b">UMS_SCHEDULER_STARTUP_INFO</a> structure passed to the <a href="https://msdn.microsoft.com/792bd7fa-0ae9-4c38-a664-5fb3e3d0c52b">EnterUmsSchedulingMode</a> function that triggered the entry point call. 

If the <i>Reason</i> parameter is <b>UmsSchedulerThreadYield</b> this parameter is the SchedulerParam parameter passed to the <a href="https://msdn.microsoft.com/d7c94ed5-9536-4c39-8658-27e4237cc9ba">UmsThreadYield</a> function that triggered the entry point call. 

If the <i>Reason</i> parameter is <b>UmsSchedulerThreadBlocked</b>, this parameter is NULL.


## -returns



This function does not return a value.




## -remarks



The <i>UmsSchedulerProc</i> function pointer type is defined as <b>PUMS_SCHEDULER_ENTRY_POINT</b> in WinBase.h. The underlying function type is defined as <b>RTL_UMS_SCHEDULER_ENTRY_POINT</b> in WinNT.h

Each UMS scheduler thread has an associated <i>UmsSchedulerProc</i> entry point function that is specified when the thread calls the <a href="https://msdn.microsoft.com/792bd7fa-0ae9-4c38-a664-5fb3e3d0c52b">EnterUmsSchedulingMode</a> function. The system calls the scheduler entry point function with a reason of <b>UmsSchedulerStartup</b> when the scheduler thread is converted for UMS.  

Subsequently, when a UMS worker thread that is running on the scheduler thread yields or blocks, the system calls the scheduler thread's entry point function with a pointer to the UMS thread context of the worker thread.

The application's scheduler is responsible for selecting the next UMS worker thread to run. The scheduler implements all policies that influence execution of its UMS threads, including processor affinity and thread priority. For example, a scheduler might give priority to I/O-intensive threads, or it might run threads on a first-come, first-served basis. This logic can be implemented in the scheduler entry point function or elsewhere in the application.

When a blocked UMS worker thread becomes unblocked, the system queues the unblocked thread to the associated completion list and signals the completion list event. To retrieve UMS worker threads from the completion list, use the <a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a> function.




## -see-also




<a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a>



<a href="https://msdn.microsoft.com/792bd7fa-0ae9-4c38-a664-5fb3e3d0c52b">EnterUmsSchedulingMode</a>



<a href="https://msdn.microsoft.com/d7c94ed5-9536-4c39-8658-27e4237cc9ba">UmsThreadYield</a>
 

 

