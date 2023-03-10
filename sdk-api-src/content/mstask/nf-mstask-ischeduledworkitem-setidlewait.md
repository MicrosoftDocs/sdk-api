---
UID: NF:mstask.IScheduledWorkItem.SetIdleWait
title: IScheduledWorkItem::SetIdleWait (mstask.h)
description: Sets the minutes that the system must be idle before the work item can run.
helpviewer_keywords: ["IScheduledWorkItem interface [Task Scheduler]","SetIdleWait method","IScheduledWorkItem.SetIdleWait","IScheduledWorkItem::SetIdleWait","SetIdleWait","SetIdleWait method [Task Scheduler]","SetIdleWait method [Task Scheduler]","IScheduledWorkItem interface","_msb_ischeduledworkitem_setidlewait","mstask/IScheduledWorkItem::SetIdleWait","taskschd.ischeduledworkitem_setidlewait"]
old-location: taskschd\ischeduledworkitem_setidlewait.htm
tech.root: taskschd
ms.assetid: f7ad639a-4094-4621-9add-b89958c0bda4
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetIdleWait method, IScheduledWorkItem.SetIdleWait, IScheduledWorkItem::SetIdleWait, SetIdleWait, SetIdleWait method [Task Scheduler], SetIdleWait method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_setidlewait, mstask/IScheduledWorkItem::SetIdleWait, taskschd.ischeduledworkitem_setidlewait
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
 - IScheduledWorkItem::SetIdleWait
 - mstask/IScheduledWorkItem::SetIdleWait
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
 - IScheduledWorkItem.SetIdleWait
---

# IScheduledWorkItem::SetIdleWait


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the minutes that the system must be idle before the <a href="/windows/desktop/TaskSchd/w">work item</a> can run.

## -parameters

### -param wIdleMinutes [in]

A value that specifies how long, in minutes, the system must remain idle before the work item can run.

### -param wDeadlineMinutes [in]

A value that specifies the maximum number of minutes that the Task Scheduler will wait for the idle-time period returned in <i>pwIdleMinutes</i>.

## -returns

The 
<b>SetIdleWait</b> method returns S_OK.

## -remarks

The idle time specified here is used in conjunction with <a href="/windows/desktop/TaskSchd/i">idle triggers</a> and <a href="/windows/desktop/TaskSchd/i">idle conditions</a>. For more information, see <a href="/windows/desktop/TaskSchd/task-idle-conditions">Task Idle Conditions</a>. Idle triggers are event-based triggers that are not associated with a scheduled time. Idle conditions, in contrast, are associated with the scheduled start time for the task.

You specify idle triggers by setting the TASK_TRIGGER_TYPE member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> to TASK_EVENT_TRIGGER_ON_IDLE. The idle trigger is fired when the system becomes idle for the amount of time specified by <i>wIdleMinutes</i>.

You set idle conditions by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a>. If the TASK_FLAG_START_ONLY_IF_IDLE flag is set, the work item runs at its scheduled time only if the system becomes idle for the amount of time specified by <i>wIdleMinutes</i>. The Task Scheduler service will wait up to the number of minutes specified in <i>wDeadlineMinutes</i> past the scheduled start time to see if the system becomes idle.

Applications must call the <b>IPersistFile::Save</b> method after calling 
<b>SetIdleWait</b> to update the idle wait interval.


#### Examples

For an example of how to set the idle wait time when creating an idle trigger, see <a href="/windows/desktop/TaskSchd/creating-an-idle-trigger-example">Creating an Idle Trigger Example</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getidlewait">IScheduledWorkItem::GetIdleWait</a>