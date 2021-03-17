---
UID: NS:mstask._TASK_TRIGGER
title: TASK_TRIGGER (mstask.h)
description: Defines the times to run a scheduled work item.
helpviewer_keywords: ["*PTASK_TRIGGER","PTASK_TRIGGER","PTASK_TRIGGER structure pointer [Task Scheduler]","TASK_TRIGGER","TASK_TRIGGER structure [Task Scheduler]","_msb_task_trigger","mstask/PTASK_TRIGGER","mstask/TASK_TRIGGER","taskschd.task_trigger","triggers [Task Scheduler]","structures","TASK_TRIGGER"]
old-location: taskschd\task_trigger.htm
tech.root: taskschd
ms.assetid: b4716e32-7c7a-40ab-baa1-4c7ebafc3d71
ms.date: 12/05/2018
ms.keywords: '*PTASK_TRIGGER, PTASK_TRIGGER, PTASK_TRIGGER structure pointer [Task Scheduler], TASK_TRIGGER, TASK_TRIGGER structure [Task Scheduler], _msb_task_trigger, mstask/PTASK_TRIGGER, mstask/TASK_TRIGGER, taskschd.task_trigger, triggers [Task Scheduler],structures,TASK_TRIGGER'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TASK_TRIGGER, *PTASK_TRIGGER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_TRIGGER
 - mstask/_TASK_TRIGGER
 - PTASK_TRIGGER
 - mstask/PTASK_TRIGGER
 - TASK_TRIGGER
 - mstask/TASK_TRIGGER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstask.h
api_name:
 - TASK_TRIGGER
---

# TASK_TRIGGER structure


## -description

Defines the times to run a scheduled <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -struct-fields

### -field cbTriggerSize

Size of this structure, in bytes.

### -field Reserved1

For internal use only; this value must be zero.

### -field wBeginYear

Year that the task trigger activates. This value must be four digits (1997, not 97). The beginning year must be specified when setting a task.

### -field wBeginMonth

Month of the year (specified in the <b>wBeginYear</b> member) that the task trigger activates. The beginning month must be specified when setting a task.

### -field wBeginDay

Day of the month (specified in the <b>wBeginMonth</b> member) that the task trigger activates. The beginning day must be specified when setting a task.

### -field wEndYear

Year that the task trigger deactivates. This value must be four digits (1997, not 97).

### -field wEndMonth

Month of the year (specified in the <b>wEndYear</b> member) that the task trigger deactivates.

### -field wEndDay

Day of the month (specified in the <b>wEndMonth</b> member) that the task trigger deactivates.

### -field wStartHour

Hour of the day the task runs. This value is on a 24-hour clock; hours go from 00 to 23.

### -field wStartMinute

Minute of the hour (specified in the <b>wStartHour</b> member) that the task runs.

### -field MinutesDuration

Number of minutes after the task starts that the trigger will remain active. The number of minutes specified here must be greater than or equal to the <b>MinutesInterval</b> setting. 




For example, if you start a task at 8:00 A.M. and want to repeatedly start the task until 5:00 P.M., there would be 540 minutes in the duration.

### -field MinutesInterval

Number of minutes between consecutive task executions. This number is counted from the start of the previous scheduled task. The number of minutes specified here must be less than the <b>MinutesDuration</b> setting. 




For example, to run a task every hour from 8:00 A.M. to 5:00 P.M., set this field to 60.

### -field rgFlags

Value that describes the behavior of the trigger. This value is a combination of the following flags. 







#### TASK_TRIGGER_FLAG_HAS_END_DATE

Trigger structure's end date is valid. If this flag is not set, the end date data is ignored and the trigger will be valid indefinitely.



#### TASK_TRIGGER_FLAG_KILL_AT_DURATION_END

Task will be terminated at the end of the active trigger's lifetime. At the duration end, the Task Scheduler sends a WM_CLOSE message to the associated application. If WM_CLOSE cannot be sent (for example, the application has no windows) or the application has not exited within three minutes of the receiving WM_CLOSE, the Task Scheduler terminates the application using <b>TerminateProcess</b>.



#### TASK_TRIGGER_FLAG_DISABLED

Task trigger is inactive.

### -field TriggerType

A 
<a href="/windows/desktop/api/mstask/ne-mstask-task_trigger_type">TASK_TRIGGER_TYPE</a> enumerated value that specifies the type of trigger. This member is used with <b>Type</b>. The type of trigger specified here determines which fields of the 
<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a> specified in <b>Type</b> member will be used. Trigger type is based on when the trigger will run the task.

### -field Type

A 
<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a> structure that specifies details about the trigger. Note that the <b>TriggerType</b> member determines which fields of the TRIGGER_TYPE_UNION union will be used.

### -field Reserved2

For internal use only; this value must be zero.

### -field wRandomMinutesInterval

Not currently used.

## -remarks

These times may include the start time, end time, duration, and modification flags for the work item. Note that when setting a trigger, the beginning day month and year must be set.

<div class="alert"><b>Note</b>  A scheduled work item can have one or more triggers defined. The times that the work item will run is the union of all the triggers defined for that item.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-createtrigger">IScheduledWorkItem::CreateTrigger</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itasktrigger-gettrigger">ITaskTrigger::GetTrigger</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itasktrigger-settrigger">ITaskTrigger::SetTrigger</a>



<a href="/windows/desktop/api/mstask/ne-mstask-task_trigger_type">TASK_TRIGGER_TYPE</a>



<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a>



<a href="/windows/desktop/TaskSchd/trigger-interfaces">Task Scheduler 2.0 Trigger Interfaces</a>