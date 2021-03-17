---
UID: NN:taskschd.ITimeTrigger
title: ITimeTrigger (taskschd.h)
description: Represents a trigger that starts a task at a specific date and time.
helpviewer_keywords: ["ITimeTrigger","ITimeTrigger interface [Task Scheduler]","ITimeTrigger interface [Task Scheduler]","described","taskschd.itimetrigger","taskschd/ITimeTrigger","time trigger [Task Scheduler]","interface"]
old-location: taskschd\itimetrigger.htm
tech.root: taskschd
ms.assetid: 4ebd5470-0801-42ff-a0c2-4d1e7f7ee365
ms.date: 12/05/2018
ms.keywords: ITimeTrigger, ITimeTrigger interface [Task Scheduler], ITimeTrigger interface [Task Scheduler],described, taskschd.itimetrigger, taskschd/ITimeTrigger, time trigger [Task Scheduler],interface
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
 - ITimeTrigger
 - taskschd/ITimeTrigger
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
 - ITimeTrigger
---

# ITimeTrigger interface


## -description

Represents a trigger that starts a task at a specific date and time.

## -remarks

The <a href="/windows/desktop/TaskSchd/taskschedulerschema-startboundary-triggerbasetype-element">StartBoundary</a> element is a required element for time and calendar triggers (<a href="/windows/desktop/TaskSchd/taskschedulerschema-timetrigger-triggergroup-element">TimeTrigger</a> and <a href="/windows/desktop/TaskSchd/taskschedulerschema-calendartrigger-triggergroup-element">CalendarTrigger</a>).

When reading or writing  XML for a task, an idle trigger is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-timetrigger-triggergroup-element">TimeTrigger</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>