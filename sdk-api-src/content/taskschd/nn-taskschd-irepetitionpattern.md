---
UID: NN:taskschd.IRepetitionPattern
title: IRepetitionPattern
author: windows-sdk-content
description: Defines how often the task is run and how long the repetition pattern is repeated after the task is started.
old-location: taskschd\irepetitionpattern.htm
tech.root: TaskSchd
ms.assetid: 7eea143b-d2f8-44d2-a3ec-8328a0bc69ef
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IRepetitionPattern, IRepetitionPattern interface [Task Scheduler], IRepetitionPattern interface [Task Scheduler],described, repetition pattern [Task Scheduler],interface, taskschd.irepetitionpattern, taskschd/IRepetitionPattern, triggers [Task Scheduler],repetition pattern interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IRepetitionPattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

When reading or writing  XML for a task, the repetition pattern is specified using the <a href="https://msdn.microsoft.com/d43c7f9a-3a7b-44a9-901b-9ad18c027b1b">Repetition</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this property, see <a href="https://msdn.microsoft.com/f1038142-b83e-4159-9a7b-db2ae4ed3bd2">Daily Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/8c3c5cc8-64aa-4706-a00a-0218fc1ae62b">Repetition Property of ITrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

