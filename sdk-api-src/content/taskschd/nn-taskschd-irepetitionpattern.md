---
UID: NN:taskschd.IRepetitionPattern
title: IRepetitionPattern (taskschd.h)
description: Defines how often the task is run and how long the repetition pattern is repeated after the task is started.
helpviewer_keywords: ["IRepetitionPattern","IRepetitionPattern interface [Task Scheduler]","IRepetitionPattern interface [Task Scheduler]","described","repetition pattern [Task Scheduler]","interface","taskschd.irepetitionpattern","taskschd/IRepetitionPattern","triggers [Task Scheduler]","repetition pattern interface"]
old-location: taskschd\irepetitionpattern.htm
tech.root: taskschd
ms.assetid: 7eea143b-d2f8-44d2-a3ec-8328a0bc69ef
ms.date: 12/05/2018
ms.keywords: IRepetitionPattern, IRepetitionPattern interface [Task Scheduler], IRepetitionPattern interface [Task Scheduler],described, repetition pattern [Task Scheduler],interface, taskschd.irepetitionpattern, taskschd/IRepetitionPattern, triggers [Task Scheduler],repetition pattern interface
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
 - IRepetitionPattern
 - taskschd/IRepetitionPattern
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
 - IRepetitionPattern
---

# IRepetitionPattern interface


## -description

Defines how often the task is run and how long the repetition pattern is repeated after the task is started.

## -remarks

If you specify a repetition duration for a task, you must also specify the repetition interval.

If you register a task that contains a  trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times. The five repetitions can be defined by the following pattern.

<ol>
<li>A task  starts at the beginning of the first minute.</li>
<li>The next task starts at the end of the first minute.</li>
<li>The next task starts at the end of the second minute.</li>
<li>The next task starts at the end of the third minute.</li>
<li>The next task starts at the end of the fourth minute.</li>
</ol>
<b>Windows Server 2003, Windows XP and Windows 2000:  </b>If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.

When reading or writing  XML for a task, the repetition pattern is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-repetition-triggerbasetype-element">Repetition</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this property, see <a href="/windows/desktop/TaskSchd/daily-trigger-example--c---">Daily Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition">Repetition Property of ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>