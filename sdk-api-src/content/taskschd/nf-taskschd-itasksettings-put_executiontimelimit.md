---
UID: NF:taskschd.ITaskSettings.put_ExecutionTimeLimit
title: ITaskSettings::put_ExecutionTimeLimit (taskschd.h)
description: Gets or sets the amount of time that is allowed to complete the task. (Put)
helpviewer_keywords: ["ExecutionTimeLimit property [Task Scheduler]","ExecutionTimeLimit property [Task Scheduler]","ITaskSettings interface","ITaskSettings interface [Task Scheduler]","ExecutionTimeLimit property","ITaskSettings.ExecutionTimeLimit","ITaskSettings.put_ExecutionTimeLimit","ITaskSettings::ExecutionTimeLimit","ITaskSettings::get_ExecutionTimeLimit","ITaskSettings::put_ExecutionTimeLimit","put_ExecutionTimeLimit","taskschd.itasksettings_executiontimelimit","taskschd/ITaskSettings::ExecutionTimeLimit","taskschd/ITaskSettings::get_ExecutionTimeLimit","taskschd/ITaskSettings::put_ExecutionTimeLimit"]
old-location: taskschd\itasksettings_executiontimelimit.htm
tech.root: taskschd
ms.assetid: 33e70133-9dfe-402a-9a1a-87f3fcc3eb96
ms.date: 12/05/2018
ms.keywords: ExecutionTimeLimit property [Task Scheduler], ExecutionTimeLimit property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],ExecutionTimeLimit property, ITaskSettings.ExecutionTimeLimit, ITaskSettings.put_ExecutionTimeLimit, ITaskSettings::ExecutionTimeLimit, ITaskSettings::get_ExecutionTimeLimit, ITaskSettings::put_ExecutionTimeLimit, put_ExecutionTimeLimit, taskschd.itasksettings_executiontimelimit, taskschd/ITaskSettings::ExecutionTimeLimit, taskschd/ITaskSettings::get_ExecutionTimeLimit, taskschd/ITaskSettings::put_ExecutionTimeLimit
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
 - ITaskSettings::put_ExecutionTimeLimit
 - taskschd/ITaskSettings::put_ExecutionTimeLimit
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
 - ITaskSettings.ExecutionTimeLimit
 - ITaskSettings.get_ExecutionTimeLimit
 - ITaskSettings.put_ExecutionTimeLimit
---

# ITaskSettings::put_ExecutionTimeLimit


## -description

Gets or sets the amount of time that is allowed to complete the task. By default, a task will be stopped 72 hours after it starts to run.  You can change this by changing this setting.

This property is read/write.

## -parameters

## -remarks

The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes). A value of PT0S will enable the task to run indefinitely.

<div class="alert"><b>Note</b>  If a task is started on demand, the ExecutionTimeLimit setting is bypassed.  Therefore, a task that is started on demand will not be terminated if it exceeds the ExecutionTimeLimit.</div>
<div> </div>
When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-executiontimelimit-settingstype-element">ExecutionTimeLimit</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
