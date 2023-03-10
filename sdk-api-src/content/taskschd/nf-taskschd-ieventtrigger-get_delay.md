---
UID: NF:taskschd.IEventTrigger.get_Delay
title: IEventTrigger::get_Delay (taskschd.h)
description: Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started. (Get)
helpviewer_keywords: ["Delay property [Task Scheduler]","Delay property [Task Scheduler]","IEventTrigger interface","IEventTrigger interface [Task Scheduler]","Delay property","IEventTrigger.Delay","IEventTrigger.get_Delay","IEventTrigger::Delay","IEventTrigger::get_Delay","IEventTrigger::put_Delay","get_Delay","taskschd.ieventtrigger_delay","taskschd/IEventTrigger::Delay","taskschd/IEventTrigger::get_Delay","taskschd/IEventTrigger::put_Delay"]
old-location: taskschd\ieventtrigger_delay.htm
tech.root: taskschd
ms.assetid: 2731ad62-6384-4c66-b66f-b159a5b15cb1
ms.date: 12/05/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler],IEventTrigger interface, IEventTrigger interface [Task Scheduler],Delay property, IEventTrigger.Delay, IEventTrigger.get_Delay, IEventTrigger::Delay, IEventTrigger::get_Delay, IEventTrigger::put_Delay, get_Delay, taskschd.ieventtrigger_delay, taskschd/IEventTrigger::Delay, taskschd/IEventTrigger::get_Delay, taskschd/IEventTrigger::put_Delay
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
 - IEventTrigger::get_Delay
 - taskschd/IEventTrigger::get_Delay
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
 - IEventTrigger.Delay
 - IEventTrigger.get_Delay
 - IEventTrigger.put_Delay
---

# IEventTrigger::get_Delay


## -description

Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started. The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes). 

This property is read/write.

## -parameters

## -remarks

When reading or writing your own XML for a task, the event delay is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-delay-eventtriggertype-element">Delay</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger">IEventTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
