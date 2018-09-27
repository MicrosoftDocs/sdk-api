---
UID: NN:taskschd.IMonthlyDOWTrigger
title: IMonthlyDOWTrigger
author: windows-sdk-content
description: Represents a trigger that starts a task on a monthly day-of-week schedule.
old-location: taskschd\imonthlydowtrigger.htm
tech.root: taskschd
ms.assetid: a950e4a0-1fcc-4213-bdb7-d1e1cf28fe91
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMonthlyDOWTrigger, IMonthlyDOWTrigger interface [Task Scheduler], IMonthlyDOWTrigger interface [Task Scheduler],described, monthly DOW trigger [Task Scheduler], taskschd.imonthlydowtrigger, taskschd/IMonthlyDOWTrigger, triggers [Task Scheduler],types,monthly DOW
ms.prod: windows
ms.technology: windows-sdk
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
 - IMonthlyDOWTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMonthlyDOWTrigger interface


## -description


Represents a trigger that starts a task on a monthly day-of-week schedule. For example, the task starts on every first Thursday, May through October.


## -remarks



The time of day that the task is started is set by the <a href="https://msdn.microsoft.com/749101ae-3db6-44ec-9113-95282c86c3c0">StartBoundary</a> property.

When reading or writing  XML for a task, a monthly day-of-week trigger is specified using the <a href="https://msdn.microsoft.com/7ff17bea-fa26-40c4-90fa-d94a3690e464">ScheduleByMonthDayOfWeek</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>



<a href="https://msdn.microsoft.com/70780fca-ba97-42b8-bc00-867c2761953c">ITriggerCollection::Create</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

