---
UID: NF:taskschd.ITrigger.put_Repetition
title: ITrigger::put_Repetition (taskschd.h)
description: Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.helpviewer_keywords: ["ITrigger interface [Task Scheduler]","Repetition property","ITrigger.Repetition","ITrigger.put_Repetition","ITrigger::Repetition","ITrigger::get_Repetition","ITrigger::put_Repetition","Repetition property [Task Scheduler]","Repetition property [Task Scheduler]","ITrigger interface","put_Repetition","taskschd.itrigger_repetition","taskschd/ITrigger::Repetition","taskschd/ITrigger::get_Repetition","taskschd/ITrigger::put_Repetition"]
old-location: taskschd\itrigger_repetition.htm
tech.root: taskschd
ms.assetid: 8c3c5cc8-64aa-4706-a00a-0218fc1ae62b
ms.date: 12/05/2018
ms.keywords: ITrigger interface [Task Scheduler],Repetition property, ITrigger.Repetition, ITrigger.put_Repetition, ITrigger::Repetition, ITrigger::get_Repetition, ITrigger::put_Repetition, Repetition property [Task Scheduler], Repetition property [Task Scheduler],ITrigger interface, put_Repetition, taskschd.itrigger_repetition, taskschd/ITrigger::Repetition, taskschd/ITrigger::get_Repetition, taskschd/ITrigger::put_Repetition
f1_keywords:
- taskschd/ITrigger.Repetition
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
- ITrigger.Repetition
- ITrigger.get_Repetition
- ITrigger.put_Repetition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITrigger::put_Repetition


## -description


Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.

This property is read/write.


## -parameters


## -remarks



When reading or writing your own XML for a task, the repetition pattern for a trigger is specified in the  <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-repetition-triggerbasetype-element">Repetition</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this property, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/daily-trigger-example--c---">Daily Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern">IRepetitionPattern</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

