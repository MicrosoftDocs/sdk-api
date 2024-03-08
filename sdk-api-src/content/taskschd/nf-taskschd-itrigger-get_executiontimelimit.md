---
UID: NF:taskschd.ITrigger.get_ExecutionTimeLimit
title: ITrigger::get_ExecutionTimeLimit (taskschd.h)
description: Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run. (Get)
helpviewer_keywords: ["ExecutionTimeLimit property [Task Scheduler]","ExecutionTimeLimit property [Task Scheduler]","ITrigger interface","ITrigger interface [Task Scheduler]","ExecutionTimeLimit property","ITrigger.ExecutionTimeLimit","ITrigger.get_ExecutionTimeLimit","ITrigger::ExecutionTimeLimit","ITrigger::get_ExecutionTimeLimit","ITrigger::put_ExecutionTimeLimit","get_ExecutionTimeLimit","taskschd.itrigger_executiontimelimit","taskschd/ITrigger::ExecutionTimeLimit","taskschd/ITrigger::get_ExecutionTimeLimit","taskschd/ITrigger::put_ExecutionTimeLimit"]
old-location: taskschd\itrigger_executiontimelimit.htm
tech.root: taskschd
ms.assetid: cfd0b02b-2040-49c1-88a1-c9663c834450
ms.date: 12/05/2018
ms.keywords: ExecutionTimeLimit property [Task Scheduler], ExecutionTimeLimit property [Task Scheduler],ITrigger interface, ITrigger interface [Task Scheduler],ExecutionTimeLimit property, ITrigger.ExecutionTimeLimit, ITrigger.get_ExecutionTimeLimit, ITrigger::ExecutionTimeLimit, ITrigger::get_ExecutionTimeLimit, ITrigger::put_ExecutionTimeLimit, get_ExecutionTimeLimit, taskschd.itrigger_executiontimelimit, taskschd/ITrigger::ExecutionTimeLimit, taskschd/ITrigger::get_ExecutionTimeLimit, taskschd/ITrigger::put_ExecutionTimeLimit
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
 - ITrigger::get_ExecutionTimeLimit
 - taskschd/ITrigger::get_ExecutionTimeLimit
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
 - ITrigger.ExecutionTimeLimit
 - ITrigger.get_ExecutionTimeLimit
 - ITrigger.put_ExecutionTimeLimit
---

# ITrigger::get_ExecutionTimeLimit


## -description

Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.

This property is read/write.

## -parameters

## -remarks

The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).

When reading or writing XML for a task, the execution time limit is specified in the  <a href="/windows/desktop/TaskSchd/taskschedulerschema-executiontimelimit-triggerbasetype-element">ExecutionTimeLimit</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
