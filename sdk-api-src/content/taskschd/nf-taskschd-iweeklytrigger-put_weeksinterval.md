---
UID: NF:taskschd.IWeeklyTrigger.put_WeeksInterval
title: IWeeklyTrigger::put_WeeksInterval (taskschd.h)
description: Gets or sets the interval between the weeks in the schedule. (Put)
helpviewer_keywords: ["IWeeklyTrigger interface [Task Scheduler]","WeeksInterval property","IWeeklyTrigger.WeeksInterval","IWeeklyTrigger.put_WeeksInterval","IWeeklyTrigger::WeeksInterval","IWeeklyTrigger::get_WeeksInterval","IWeeklyTrigger::put_WeeksInterval","WeeksInterval property [Task Scheduler]","WeeksInterval property [Task Scheduler]","IWeeklyTrigger interface","put_WeeksInterval","taskschd.iweeklytrigger_weeksinterval","taskschd/IWeeklyTrigger::WeeksInterval","taskschd/IWeeklyTrigger::get_WeeksInterval","taskschd/IWeeklyTrigger::put_WeeksInterval"]
old-location: taskschd\iweeklytrigger_weeksinterval.htm
tech.root: taskschd
ms.assetid: 11f2c708-a95b-4b9c-a3a6-9b37b01d2d0b
ms.date: 12/05/2018
ms.keywords: IWeeklyTrigger interface [Task Scheduler],WeeksInterval property, IWeeklyTrigger.WeeksInterval, IWeeklyTrigger.put_WeeksInterval, IWeeklyTrigger::WeeksInterval, IWeeklyTrigger::get_WeeksInterval, IWeeklyTrigger::put_WeeksInterval, WeeksInterval property [Task Scheduler], WeeksInterval property [Task Scheduler],IWeeklyTrigger interface, put_WeeksInterval, taskschd.iweeklytrigger_weeksinterval, taskschd/IWeeklyTrigger::WeeksInterval, taskschd/IWeeklyTrigger::get_WeeksInterval, taskschd/IWeeklyTrigger::put_WeeksInterval
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
 - IWeeklyTrigger::put_WeeksInterval
 - taskschd/IWeeklyTrigger::put_WeeksInterval
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
 - IWeeklyTrigger.WeeksInterval
 - IWeeklyTrigger.get_WeeksInterval
 - IWeeklyTrigger.put_WeeksInterval
---

# IWeeklyTrigger::put_WeeksInterval


## -description

Gets or sets the interval between the weeks in the schedule.

This property is read/write.

## -parameters

## -remarks

An interval of 1 produces a weekly schedule. An interval of 2 produces an every-other week schedule.

When reading or writing your own XML for a task, the interval for a weekly schedule is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-weeksinterval-weeklyscheduletype-element">WeeksInterval</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger">IWeeklyTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
