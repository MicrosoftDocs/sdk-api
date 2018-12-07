---
UID: NN:taskschd.IDailyTrigger
title: IDailyTrigger
author: windows-sdk-content
description: Represents a trigger that starts a task based on a daily schedule.
old-location: taskschd\idailytrigger.htm
tech.root: taskschd
ms.assetid: 9980ddb1-9873-46d2-8dea-bfc3fd78bba8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDailyTrigger, IDailyTrigger interface [Task Scheduler], IDailyTrigger interface [Task Scheduler],described, daily trigger [Task Scheduler],interface, taskschd.idailytrigger, taskschd/IDailyTrigger
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
 - IDailyTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDailyTrigger interface


## -description


Represents a trigger that starts a task based on a daily schedule. For example, the task starts at a specific time every day, every other day, every third day, and so on.


## -remarks



The time of day that the task is started is set by the <a href="https://msdn.microsoft.com/749101ae-3db6-44ec-9113-95282c86c3c0">StartBoundary</a> property.

An interval of 1 produces a daily schedule. An interval of 2 produces an every other day schedule and so on.

When reading or writing your own XML for a task, a daily trigger is specified using the <a href="https://msdn.microsoft.com/5a6097ce-a855-4b08-84c5-71f06343805e">ScheduleByDay</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/f1038142-b83e-4159-9a7b-db2ae4ed3bd2">Daily Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>



<a href="https://msdn.microsoft.com/70780fca-ba97-42b8-bc00-867c2761953c">ITriggerCollection::Create</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

