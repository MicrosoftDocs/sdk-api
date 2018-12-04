---
UID: NN:taskschd.IWeeklyTrigger
title: IWeeklyTrigger
author: windows-sdk-content
description: Represents a trigger that starts a task based on a weekly schedule.
old-location: taskschd\iweeklytrigger.htm
tech.root: taskschd
ms.assetid: c10b050a-8319-4e21-85aa-0bceb76abaaf
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWeeklyTrigger, IWeeklyTrigger interface [Task Scheduler], IWeeklyTrigger interface [Task Scheduler],described, taskschd.iweeklytrigger, taskschd/IWeeklyTrigger, weekly trigger [Task Scheduler],interface
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
 - IWeeklyTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWeeklyTrigger interface


## -description


Represents a trigger that starts a task based on a weekly schedule. For example, the task starts at 8:00 A.M. on a specific day of the week every week or every other week.


## -remarks



The time of day that the task is started is set by the <a href="https://msdn.microsoft.com/749101ae-3db6-44ec-9113-95282c86c3c0">StartBoundary</a> property.

When reading or writing your own XML for a task, a weekly trigger is specified using the <a href="https://msdn.microsoft.com/d2c33e76-0564-4b3c-ab86-e7bca667fa4f">ScheduleByWeek</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>



<a href="https://msdn.microsoft.com/70780fca-ba97-42b8-bc00-867c2761953c">ITriggerCollection::Create</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

