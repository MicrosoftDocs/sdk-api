---
UID: NN:taskschd.IMonthlyTrigger
title: IMonthlyTrigger (taskschd.h)
description: Represents a trigger that starts a job based on a monthly schedule.
old-location: taskschd\imonthlytrigger.htm
tech.root: taskschd
ms.assetid: 2ed206a6-22e0-4131-92ce-29536ad65c6c
ms.date: 12/05/2018
ms.keywords: IMonthlyTrigger, IMonthlyTrigger interface [Task Scheduler], IMonthlyTrigger interface [Task Scheduler],described, monthly trigger [Task Scheduler],interface, taskschd.imonthlytrigger, taskschd/IMonthlyTrigger
f1_keywords:
- taskschd/IMonthlyTrigger
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
- IMonthlyTrigger
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMonthlyTrigger interface


## -description


Represents a trigger that starts a job based on a monthly schedule.  For example, the task starts on specific days of specific months.


## -remarks



The time of day that the task is started is set by the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary">StartBoundary</a> property.

When reading or writing your own XML for a task, a monthly trigger is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-schedulebymonth-calendartriggertype-element">ScheduleByMonth </a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">ITriggerCollection::Create</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

