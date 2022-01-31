---
UID: NE:mstask._TASK_TRIGGER_TYPE
title: TASK_TRIGGER_TYPE (mstask.h)
description: Defines the types of triggers associated with a task.
helpviewer_keywords: ["*PTASK_TRIGGER_TYPE","PTASK_TRIGGER_TYPE","PTASK_TRIGGER_TYPE enumeration pointer [Task Scheduler]","TASK_EVENT_TRIGGER_AT_LOGON","TASK_EVENT_TRIGGER_AT_SYSTEMSTART","TASK_EVENT_TRIGGER_ON_IDLE","TASK_TIME_TRIGGER_DAILY","TASK_TIME_TRIGGER_MONTHLYDATE","TASK_TIME_TRIGGER_MONTHLYDOW","TASK_TIME_TRIGGER_ONCE","TASK_TIME_TRIGGER_WEEKLY","TASK_TRIGGER_TYPE","TASK_TRIGGER_TYPE enumeration [Task Scheduler]","_msb_task_trigger_type","mstask/PTASK_TRIGGER_TYPE","mstask/TASK_EVENT_TRIGGER_AT_LOGON","mstask/TASK_EVENT_TRIGGER_AT_SYSTEMSTART","mstask/TASK_EVENT_TRIGGER_ON_IDLE","mstask/TASK_TIME_TRIGGER_DAILY","mstask/TASK_TIME_TRIGGER_MONTHLYDATE","mstask/TASK_TIME_TRIGGER_MONTHLYDOW","mstask/TASK_TIME_TRIGGER_ONCE","mstask/TASK_TIME_TRIGGER_WEEKLY","mstask/TASK_TRIGGER_TYPE","taskschd.task_trigger_type"]
old-location: taskschd\task_trigger_type.htm
tech.root: taskschd
ms.assetid: 07cba55c-47af-4879-b7be-12952763e016
ms.date: 12/05/2018
ms.keywords: '*PTASK_TRIGGER_TYPE, PTASK_TRIGGER_TYPE, PTASK_TRIGGER_TYPE enumeration pointer [Task Scheduler], TASK_EVENT_TRIGGER_AT_LOGON, TASK_EVENT_TRIGGER_AT_SYSTEMSTART, TASK_EVENT_TRIGGER_ON_IDLE, TASK_TIME_TRIGGER_DAILY, TASK_TIME_TRIGGER_MONTHLYDATE, TASK_TIME_TRIGGER_MONTHLYDOW, TASK_TIME_TRIGGER_ONCE, TASK_TIME_TRIGGER_WEEKLY, TASK_TRIGGER_TYPE, TASK_TRIGGER_TYPE enumeration [Task Scheduler], _msb_task_trigger_type, mstask/PTASK_TRIGGER_TYPE, mstask/TASK_EVENT_TRIGGER_AT_LOGON, mstask/TASK_EVENT_TRIGGER_AT_SYSTEMSTART, mstask/TASK_EVENT_TRIGGER_ON_IDLE, mstask/TASK_TIME_TRIGGER_DAILY, mstask/TASK_TIME_TRIGGER_MONTHLYDATE, mstask/TASK_TIME_TRIGGER_MONTHLYDOW, mstask/TASK_TIME_TRIGGER_ONCE, mstask/TASK_TIME_TRIGGER_WEEKLY, mstask/TASK_TRIGGER_TYPE, taskschd.task_trigger_type'
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
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_TRIGGER_TYPE
 - mstask/_TASK_TRIGGER_TYPE
 - PTASK_TRIGGER_TYPE
 - mstask/PTASK_TRIGGER_TYPE
 - TASK_TRIGGER_TYPE
 - mstask/TASK_TRIGGER_TYPE
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
 - TASK_TRIGGER_TYPE
---

# TASK_TRIGGER_TYPE enumeration


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the  <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-enumerated-types">Task Scheduler 2.0 Enumerated Types</a> instead.] ]

Defines the types of <a href="/windows/desktop/TaskSchd/t">triggers</a> associated with a task.

## -enum-fields

### -field TASK_TIME_TRIGGER_ONCE:0

Trigger is set to run the task a single time. 




When this value is specified, the <b>Type</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure is ignored.

### -field TASK_TIME_TRIGGER_DAILY:1

Trigger is set to run the task on a daily interval. 




When this value is specified, the 
<b>DAILY</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a> structure is used.

### -field TASK_TIME_TRIGGER_WEEKLY:2

Trigger is set to run the work item on specific days of a specific week of a specific month. 




When this value is specified, the 
<b>WEEKLY</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a> structure is used.

### -field TASK_TIME_TRIGGER_MONTHLYDATE:3

Trigger is set to run the task on a specific day(s) of the month. 




When this value is specified, the 
<b>MONTHLYDATE</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a> structure is used.

### -field TASK_TIME_TRIGGER_MONTHLYDOW:4

Trigger is set to run the task on specific days, weeks, and months. 




When this value is specified, the 
<b>MONTHLYDOW</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a> structure is used.

### -field TASK_EVENT_TRIGGER_ON_IDLE:5

Trigger is set to run the task if the system remains idle for the amount of time specified by the <a href="/windows/desktop/TaskSchd/i">idle wait time</a> of the task. 




When this value is specified, the <b>wStartHour</b>, <b>wStartMinute</b>, and <b>Type</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure are ignored.

### -field TASK_EVENT_TRIGGER_AT_SYSTEMSTART:6

Trigger is set to run the task at system startup. 




When this value is specified, the <b>Type</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure is ignored.

### -field TASK_EVENT_TRIGGER_AT_LOGON:7

Trigger is set to run the task when a user logs on. 




When this value is specified, the <b>Type</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure is ignored.

## -remarks

The constants defined here are used in the <b>TriggerType</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure.

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setidlewait">IScheduledWorkItem::SetIdleWait</a>



<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a>



<a href="/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2">TASK_TRIGGER_TYPE2</a>



<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
