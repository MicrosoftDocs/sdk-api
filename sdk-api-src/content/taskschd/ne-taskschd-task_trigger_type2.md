---
UID: NE:taskschd._TASK_TRIGGER_TYPE2
title: TASK_TRIGGER_TYPE2 (taskschd.h)
description: Defines the type of triggers that can be used by tasks.
helpviewer_keywords: ["TASK_TRIGGER_BOOT","TASK_TRIGGER_DAILY","TASK_TRIGGER_EVENT","TASK_TRIGGER_IDLE","TASK_TRIGGER_LOGON","TASK_TRIGGER_MONTHLY","TASK_TRIGGER_MONTHLYDOW","TASK_TRIGGER_REGISTRATION","TASK_TRIGGER_SESSION_STATE_CHANGE","TASK_TRIGGER_TIME","TASK_TRIGGER_TYPE2","TASK_TRIGGER_TYPE2 enumeration [Task Scheduler]","TASK_TRIGGER_WEEKLY","taskschd.triggertype","taskschd/TASK_TRIGGER_BOOT","taskschd/TASK_TRIGGER_DAILY","taskschd/TASK_TRIGGER_EVENT","taskschd/TASK_TRIGGER_IDLE","taskschd/TASK_TRIGGER_LOGON","taskschd/TASK_TRIGGER_MONTHLY","taskschd/TASK_TRIGGER_MONTHLYDOW","taskschd/TASK_TRIGGER_REGISTRATION","taskschd/TASK_TRIGGER_SESSION_STATE_CHANGE","taskschd/TASK_TRIGGER_TIME","taskschd/TASK_TRIGGER_TYPE2","taskschd/TASK_TRIGGER_WEEKLY"]
old-location: taskschd\triggertype.htm
tech.root: taskschd
ms.assetid: 489015a1-5a3c-4994-aa1f-bc02dfff149d
ms.date: 12/05/2018
ms.keywords: TASK_TRIGGER_BOOT, TASK_TRIGGER_DAILY, TASK_TRIGGER_EVENT, TASK_TRIGGER_IDLE, TASK_TRIGGER_LOGON, TASK_TRIGGER_MONTHLY, TASK_TRIGGER_MONTHLYDOW, TASK_TRIGGER_REGISTRATION, TASK_TRIGGER_SESSION_STATE_CHANGE, TASK_TRIGGER_TIME, TASK_TRIGGER_TYPE2, TASK_TRIGGER_TYPE2 enumeration [Task Scheduler], TASK_TRIGGER_WEEKLY, taskschd.triggertype, taskschd/TASK_TRIGGER_BOOT, taskschd/TASK_TRIGGER_DAILY, taskschd/TASK_TRIGGER_EVENT, taskschd/TASK_TRIGGER_IDLE, taskschd/TASK_TRIGGER_LOGON, taskschd/TASK_TRIGGER_MONTHLY, taskschd/TASK_TRIGGER_MONTHLYDOW, taskschd/TASK_TRIGGER_REGISTRATION, taskschd/TASK_TRIGGER_SESSION_STATE_CHANGE, taskschd/TASK_TRIGGER_TIME, taskschd/TASK_TRIGGER_TYPE2, taskschd/TASK_TRIGGER_WEEKLY
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TASK_TRIGGER_TYPE2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_TRIGGER_TYPE2
 - taskschd/_TASK_TRIGGER_TYPE2
 - TASK_TRIGGER_TYPE2
 - taskschd/TASK_TRIGGER_TYPE2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - taskschd.h
api_name:
 - TASK_TRIGGER_TYPE2
---

# TASK_TRIGGER_TYPE2 enumeration


## -description

Defines the type of triggers that can be used by tasks.

## -enum-fields

### -field TASK_TRIGGER_EVENT:0

Triggers the task when a specific event occurs. For more information about event triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger">IEventTrigger</a>.

### -field TASK_TRIGGER_TIME:1

Triggers the task at a specific time of day. For more information about time triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-itimetrigger">ITimeTrigger</a>.

### -field TASK_TRIGGER_DAILY:2

Triggers the task on a daily schedule. For example, the task starts at a specific time every day, every other day, or every third day. For more information about daily triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-idailytrigger">IDailyTrigger</a>.

### -field TASK_TRIGGER_WEEKLY:3

Triggers the task on a weekly schedule. For example, the task starts at 8:00 AM on a specific day every week or other week.  For more information about weekly triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger">IWeeklyTrigger</a>.

### -field TASK_TRIGGER_MONTHLY:4

Triggers the task on a monthly schedule. For example, the task starts on specific days of specific months. For more information about monthly triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger">IMonthlyTrigger</a>.

### -field TASK_TRIGGER_MONTHLYDOW:5

Triggers the task on a monthly day-of-week schedule. For example, the task starts on a specific   days of the week, weeks of the  month, and months of the year. For more information about monthly day-of-week triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger">IMonthlyDOWTrigger</a>.

### -field TASK_TRIGGER_IDLE:6

Triggers the task when the computer goes into an idle state. For more information about idle triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-iidletrigger">IIdleTrigger</a>.

### -field TASK_TRIGGER_REGISTRATION:7

Triggers the task when the task is registered. For more information about registration triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger">IRegistrationTrigger</a>.

### -field TASK_TRIGGER_BOOT:8

Triggers the task when the computer boots.  For more information about boot triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-iboottrigger">IBootTrigger</a>.

### -field TASK_TRIGGER_LOGON:9

Triggers the task when a specific user logs on.  For more information about logon triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger">ILogonTrigger</a>.

### -field TASK_TRIGGER_SESSION_STATE_CHANGE:11

Triggers the task when a specific user session state changes.  For more information about session state change triggers, see <a href="/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger">ISessionStateChangeTrigger</a>.

### -field TASK_TRIGGER_CUSTOM_TRIGGER_01:12

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
