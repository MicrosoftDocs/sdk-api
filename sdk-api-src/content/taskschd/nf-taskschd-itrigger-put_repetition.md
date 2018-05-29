---
UID: NF:taskschd.ITrigger.put_Repetition
title: ITrigger::put_Repetition
author: windows-sdk-content
description: Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.
old-location: taskschd\itrigger_repetition.htm
old-project: TaskSchd
ms.assetid: 8c3c5cc8-64aa-4706-a00a-0218fc1ae62b
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITrigger interface [Task Scheduler],Repetition property, ITrigger.Repetition, ITrigger.put_Repetition, ITrigger::Repetition, ITrigger::get_Repetition, ITrigger::put_Repetition, Repetition property [Task Scheduler], Repetition property [Task Scheduler],ITrigger interface, put_Repetition, taskschd.itrigger_repetition, taskschd/ITrigger::Repetition, taskschd/ITrigger::get_Repetition, taskschd/ITrigger::put_Repetition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITrigger.Repetition
-	ITrigger.get_Repetition
-	ITrigger.put_Repetition
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITrigger::put_Repetition


## -description


Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.

This property is read/write.


## -parameters


## -remarks



When reading or writing your own XML for a task, the repetition pattern for a trigger is specified in the  <a href="https://msdn.microsoft.com/d43c7f9a-3a7b-44a9-901b-9ad18c027b1b">Repetition</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this property, see <a href="https://msdn.microsoft.com/f1038142-b83e-4159-9a7b-db2ae4ed3bd2">Daily Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7eea143b-d2f8-44d2-a3ec-8328a0bc69ef">IRepetitionPattern</a>



<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

