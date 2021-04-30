---
UID: NF:mstask.IScheduledWorkItem.GetIdleWait
title: IScheduledWorkItem::GetIdleWait (mstask.h)
description: Retrieves the idle wait time for the work item.
helpviewer_keywords: ["GetIdleWait","GetIdleWait method [Task Scheduler]","GetIdleWait method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetIdleWait method","IScheduledWorkItem.GetIdleWait","IScheduledWorkItem::GetIdleWait","_msb_ischeduledworkitem_getidlewait","mstask/IScheduledWorkItem::GetIdleWait","taskschd.ischeduledworkitem_getidlewait"]
old-location: taskschd\ischeduledworkitem_getidlewait.htm
tech.root: taskschd
ms.assetid: 72d53691-f2ea-4a20-8e85-f9db81f830cd
ms.date: 12/05/2018
ms.keywords: GetIdleWait, GetIdleWait method [Task Scheduler], GetIdleWait method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetIdleWait method, IScheduledWorkItem.GetIdleWait, IScheduledWorkItem::GetIdleWait, _msb_ischeduledworkitem_getidlewait, mstask/IScheduledWorkItem::GetIdleWait, taskschd.ischeduledworkitem_getidlewait
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - IScheduledWorkItem::GetIdleWait
 - mstask/IScheduledWorkItem::GetIdleWait
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem.GetIdleWait
---

# IScheduledWorkItem::GetIdleWait


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the <a href="/windows/desktop/TaskSchd/i">idle wait time</a> for the work item. 
			
For information about idle conditions, see <a href="/windows/desktop/TaskSchd/task-idle-conditions">Task Idle Conditions</a>.

## -parameters

### -param pwIdleMinutes [out]

A pointer to a <b>WORD</b> that contains the idle wait time for the current work item, in minutes.

### -param pwDeadlineMinutes [out]

A pointer to a <b>WORD</b> that specifies the maximum number of minutes that the Task Scheduler will wait for the idle-time period returned in <i>pwIdleMinutes</i>.

## -returns

The 
<b>GetIdleWait</b> method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The arguments are not valid.

</td>
</tr>
</table>

## -remarks

The idle time returned here is used in conjunction with <a href="/windows/desktop/TaskSchd/i">idle triggers</a> and <a href="/windows/desktop/TaskSchd/i">idle conditions</a>. Idle triggers are event-based triggers that are not associated with a scheduled time. Idle conditions are associated with the scheduled start time for the task.

Idle triggers are specified by setting the 
<a href="/windows/desktop/api/mstask/ne-mstask-task_trigger_type">TASK_TRIGGER_TYPE</a> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure to the value TASK_EVENT_TRIGGER_ON_IDLE. The idle trigger is fired when the system becomes idle for the amount of time returned in <i>pwIdleMinutes</i>.

You can set idle conditions by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a>. If the TASK_FLAG_START_ONLY_IF_IDLE flag is set, the work item runs at its scheduled time only if the system becomes idle for the amount of time returned in <i>pwIdleMinutes</i>. The Task Scheduler service will wait up to <i>pwDeadlineMinutes</i> past the scheduled start time to see if the system becomes idle.


#### Examples

For an example of how to retrieve the idle wait time of a task, see <a href="/windows/desktop/TaskSchd/c-c-code-example-retrieving-task-idle-wait-time">C/C++ Code Example: Retrieving Task Idle-wait Time</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setidlewait">IScheduledWorkItem::SetIdleWait</a>