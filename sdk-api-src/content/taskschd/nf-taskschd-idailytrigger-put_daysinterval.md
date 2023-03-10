---
UID: NF:taskschd.IDailyTrigger.put_DaysInterval
title: IDailyTrigger::put_DaysInterval (taskschd.h)
description: Gets or sets the interval between the days in the schedule. (Put)
helpviewer_keywords: ["DaysInterval property [Task Scheduler]","DaysInterval property [Task Scheduler]","IDailyTrigger interface","IDailyTrigger interface [Task Scheduler]","DaysInterval property","IDailyTrigger.DaysInterval","IDailyTrigger.put_DaysInterval","IDailyTrigger::DaysInterval","IDailyTrigger::get_DaysInterval","IDailyTrigger::put_DaysInterval","put_DaysInterval","taskschd.idailytrigger_daysinterval","taskschd/IDailyTrigger::DaysInterval","taskschd/IDailyTrigger::get_DaysInterval","taskschd/IDailyTrigger::put_DaysInterval"]
old-location: taskschd\idailytrigger_daysinterval.htm
tech.root: taskschd
ms.assetid: fde401c7-f0ab-46bd-9b84-bd9f762f2c89
ms.date: 12/05/2018
ms.keywords: DaysInterval property [Task Scheduler], DaysInterval property [Task Scheduler],IDailyTrigger interface, IDailyTrigger interface [Task Scheduler],DaysInterval property, IDailyTrigger.DaysInterval, IDailyTrigger.put_DaysInterval, IDailyTrigger::DaysInterval, IDailyTrigger::get_DaysInterval, IDailyTrigger::put_DaysInterval, put_DaysInterval, taskschd.idailytrigger_daysinterval, taskschd/IDailyTrigger::DaysInterval, taskschd/IDailyTrigger::get_DaysInterval, taskschd/IDailyTrigger::put_DaysInterval
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
 - IDailyTrigger::put_DaysInterval
 - taskschd/IDailyTrigger::put_DaysInterval
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
 - IDailyTrigger.DaysInterval
 - IDailyTrigger.get_DaysInterval
 - IDailyTrigger.put_DaysInterval
---

# IDailyTrigger::put_DaysInterval


## -description

Gets or sets the interval between the days in the schedule.

This property is read/write.

## -parameters

## -remarks

An interval of 1 produces a daily schedule. An interval of 2 produces an every-other day schedule.

When reading or writing your own XML for a task, the interval for a daily schedule is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-daysinterval-dailyscheduletype-element">DaysInterval</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-idailytrigger">IDailyTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
