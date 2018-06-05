---
UID: NF:taskschd.ITrigger.get_ExecutionTimeLimit
title: ITrigger::get_ExecutionTimeLimit
author: windows-sdk-content
description: Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.
old-location: taskschd\itrigger_executiontimelimit.htm
old-project: TaskSchd
ms.assetid: cfd0b02b-2040-49c1-88a1-c9663c834450
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ExecutionTimeLimit property [Task Scheduler], ExecutionTimeLimit property [Task Scheduler],ITrigger interface, ITrigger interface [Task Scheduler],ExecutionTimeLimit property, ITrigger.ExecutionTimeLimit, ITrigger.get_ExecutionTimeLimit, ITrigger::ExecutionTimeLimit, ITrigger::get_ExecutionTimeLimit, ITrigger::put_ExecutionTimeLimit, get_ExecutionTimeLimit, taskschd.itrigger_executiontimelimit, taskschd/ITrigger::ExecutionTimeLimit, taskschd/ITrigger::get_ExecutionTimeLimit, taskschd/ITrigger::put_ExecutionTimeLimit
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITrigger.ExecutionTimeLimit
-	ITrigger.get_ExecutionTimeLimit
-	ITrigger.put_ExecutionTimeLimit
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITrigger::get_ExecutionTimeLimit


## -description


Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.

This property is read/write.


## -parameters


## -remarks



The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).

When reading or writing XML for a task, the execution time limit is specified in the  <a href="https://msdn.microsoft.com/f78e7c7b-d069-4920-9435-020f6e081eff">ExecutionTimeLimit</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

