---
UID: NC:winnt.RTL_UMS_SCHEDULER_ENTRY_POINT
title: RTL_UMS_SCHEDULER_ENTRY_POINT (winnt.h)
description: The application-defined user-mode scheduling (UMS) scheduler entry point function associated with a UMS completion list.
helpviewer_keywords: ["0","1","RTL_UMS_SCHEDULER_ENTRY_POINT","RTL_UMS_SCHEDULER_ENTRY_POINT callback","UmsSchedulerProc","UmsSchedulerProc callback function","UmsSchedulerStartup","UmsSchedulerThreadBlocked","UmsSchedulerThreadYield","base.umsschedulerproc","winnt/UmsSchedulerProc"]
old-location: base\umsschedulerproc.htm
tech.root: backup
ms.assetid: 10de1c48-255d-45c3-acf0-25f8a564b585
ms.date: 12/05/2018
ms.keywords: 0, 1, RTL_UMS_SCHEDULER_ENTRY_POINT, RTL_UMS_SCHEDULER_ENTRY_POINT callback, UmsSchedulerProc, UmsSchedulerProc callback function, UmsSchedulerStartup, UmsSchedulerThreadBlocked, UmsSchedulerThreadYield, base.umsschedulerproc, winnt/UmsSchedulerProc
req.header: winnt.h
req.include-header: WinBase.h, Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RTL_UMS_SCHEDULER_ENTRY_POINT
 - winnt/RTL_UMS_SCHEDULER_ENTRY_POINT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinNT.h
api_name:
 - UmsSchedulerProc
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
A UMS scheduler thread was created. The entry point is called with this reason once each time  <a href="/windows/desktop/api/winbase/nf-winbase-enterumsschedulingmode">EnterUmsSchedulingMode</a> is called.

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
An executing UMS worker thread yielded control by calling the <a href="/windows/desktop/api/winbase/nf-winbase-umsthreadyield">UmsThreadYield</a> function. 

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

If the <i>Reason</i> parameter is <b>UmsSchedulerStartup</b>, this parameter is the <b>SchedulerParam</b> member of the <a href="/windows/desktop/api/winbase/ns-winbase-ums_scheduler_startup_info">UMS_SCHEDULER_STARTUP_INFO</a> structure passed to the <a href="/windows/desktop/api/winbase/nf-winbase-enterumsschedulingmode">EnterUmsSchedulingMode</a> function that triggered the entry point call. 

If the <i>Reason</i> parameter is <b>UmsSchedulerThreadYield</b> this parameter is the SchedulerParam parameter passed to the <a href="/windows/desktop/api/winbase/nf-winbase-umsthreadyield">UmsThreadYield</a> function that triggered the entry point call. 

If the <i>Reason</i> parameter is <b>UmsSchedulerThreadBlocked</b>, this parameter is NULL.

## -remarks

The <i>UmsSchedulerProc</i> function pointer type is defined as <b>PUMS_SCHEDULER_ENTRY_POINT</b> in WinBase.h. The underlying function type is defined as <b>RTL_UMS_SCHEDULER_ENTRY_POINT</b> in WinNT.h

Each UMS scheduler thread has an associated <i>UmsSchedulerProc</i> entry point function that is specified when the thread calls the <a href="/windows/desktop/api/winbase/nf-winbase-enterumsschedulingmode">EnterUmsSchedulingMode</a> function. The system calls the scheduler entry point function with a reason of <b>UmsSchedulerStartup</b> when the scheduler thread is converted for UMS.  

Subsequently, when a UMS worker thread that is running on the scheduler thread yields or blocks, the system calls the scheduler thread's entry point function with a pointer to the UMS thread context of the worker thread.

The application's scheduler is responsible for selecting the next UMS worker thread to run. The scheduler implements all policies that influence execution of its UMS threads, including processor affinity and thread priority. For example, a scheduler might give priority to I/O-intensive threads, or it might run threads on a first-come, first-served basis. This logic can be implemented in the scheduler entry point function or elsewhere in the application.

When a blocked UMS worker thread becomes unblocked, the system queues the unblocked thread to the associated completion list and signals the completion list event. To retrieve UMS worker threads from the completion list, use the <a href="/windows/desktop/api/winbase/nf-winbase-dequeueumscompletionlistitems">DequeueUmsCompletionListItems</a> function.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-dequeueumscompletionlistitems">DequeueUmsCompletionListItems</a>



<a href="/windows/desktop/api/winbase/nf-winbase-enterumsschedulingmode">EnterUmsSchedulingMode</a>



<a href="/windows/desktop/api/winbase/nf-winbase-umsthreadyield">UmsThreadYield</a>