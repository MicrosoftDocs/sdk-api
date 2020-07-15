---
UID: NN:taskschd.IWeeklyTrigger
title: IWeeklyTrigger (taskschd.h)
description: Represents a trigger that starts a task based on a weekly schedule.
helpviewer_keywords: ["IWeeklyTrigger","IWeeklyTrigger interface [Task Scheduler]","IWeeklyTrigger interface [Task Scheduler]","described","taskschd.iweeklytrigger","taskschd/IWeeklyTrigger","weekly trigger [Task Scheduler]","interface"]
old-location: taskschd\iweeklytrigger.htm
tech.root: taskschd
ms.assetid: c10b050a-8319-4e21-85aa-0bceb76abaaf
ms.date: 12/05/2018
ms.keywords: IWeeklyTrigger, IWeeklyTrigger interface [Task Scheduler], IWeeklyTrigger interface [Task Scheduler],described, taskschd.iweeklytrigger, taskschd/IWeeklyTrigger, weekly trigger [Task Scheduler],interface
f1_keywords:
- taskschd/IWeeklyTrigger
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- taskschd.dll
api_name:
- IWeeklyTrigger
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWeeklyTrigger interface


## -description


Represents a trigger that starts a task based on a weekly schedule. For example, the task starts at 8:00 A.M. on a specific day of the week every week or every other week.


## -remarks



The time of day that the task is started is set by the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary">StartBoundary</a> property.

When reading or writing your own XML for a task, a weekly trigger is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-schedulebyweek-calendartriggertype-element">ScheduleByWeek</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">ITriggerCollection::Create</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

