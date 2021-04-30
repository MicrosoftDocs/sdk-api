---
UID: NN:taskschd.IDailyTrigger
title: IDailyTrigger (taskschd.h)
description: Represents a trigger that starts a task based on a daily schedule.
helpviewer_keywords: ["IDailyTrigger","IDailyTrigger interface [Task Scheduler]","IDailyTrigger interface [Task Scheduler]","described","daily trigger [Task Scheduler]","interface","taskschd.idailytrigger","taskschd/IDailyTrigger"]
old-location: taskschd\idailytrigger.htm
tech.root: taskschd
ms.assetid: 9980ddb1-9873-46d2-8dea-bfc3fd78bba8
ms.date: 12/05/2018
ms.keywords: IDailyTrigger, IDailyTrigger interface [Task Scheduler], IDailyTrigger interface [Task Scheduler],described, daily trigger [Task Scheduler],interface, taskschd.idailytrigger, taskschd/IDailyTrigger
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDailyTrigger
 - taskschd/IDailyTrigger
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IDailyTrigger
---

# IDailyTrigger interface


## -description

Represents a trigger that starts a task based on a daily schedule. For example, the task starts at a specific time every day, every other day, every third day, and so on.

## -remarks

The time of day that the task is started is set by the <a href="/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary">StartBoundary</a> property.

An interval of 1 produces a daily schedule. An interval of 2 produces an every other day schedule and so on.

When reading or writing your own XML for a task, a daily trigger is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-schedulebyday-calendartriggertype-element">ScheduleByDay</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/daily-trigger-example--c---">Daily Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">ITriggerCollection::Create</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>