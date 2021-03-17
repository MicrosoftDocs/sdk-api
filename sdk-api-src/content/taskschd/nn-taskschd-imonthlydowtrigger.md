---
UID: NN:taskschd.IMonthlyDOWTrigger
title: IMonthlyDOWTrigger (taskschd.h)
description: Represents a trigger that starts a task on a monthly day-of-week schedule.
helpviewer_keywords: ["IMonthlyDOWTrigger","IMonthlyDOWTrigger interface [Task Scheduler]","IMonthlyDOWTrigger interface [Task Scheduler]","described","monthly DOW trigger [Task Scheduler]","taskschd.imonthlydowtrigger","taskschd/IMonthlyDOWTrigger","triggers [Task Scheduler]","types","monthly DOW"]
old-location: taskschd\imonthlydowtrigger.htm
tech.root: taskschd
ms.assetid: a950e4a0-1fcc-4213-bdb7-d1e1cf28fe91
ms.date: 12/05/2018
ms.keywords: IMonthlyDOWTrigger, IMonthlyDOWTrigger interface [Task Scheduler], IMonthlyDOWTrigger interface [Task Scheduler],described, monthly DOW trigger [Task Scheduler], taskschd.imonthlydowtrigger, taskschd/IMonthlyDOWTrigger, triggers [Task Scheduler],types,monthly DOW
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
 - IMonthlyDOWTrigger
 - taskschd/IMonthlyDOWTrigger
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
 - IMonthlyDOWTrigger
---

# IMonthlyDOWTrigger interface


## -description

Represents a trigger that starts a task on a monthly day-of-week schedule. For example, the task starts on every first Thursday, May through October.

## -remarks

The time of day that the task is started is set by the <a href="/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary">StartBoundary</a> property.

When reading or writing  XML for a task, a monthly day-of-week trigger is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element">ScheduleByMonthDayOfWeek</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">ITriggerCollection::Create</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>