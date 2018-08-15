---
UID: NN:taskschd.IMonthlyTrigger
title: IMonthlyTrigger
author: windows-sdk-content
description: Represents a trigger that starts a job based on a monthly schedule.
old-location: taskschd\imonthlytrigger.htm
old-project: taskschd
ms.assetid: 2ed206a6-22e0-4131-92ce-29536ad65c6c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IMonthlyTrigger, IMonthlyTrigger interface [Task Scheduler], IMonthlyTrigger interface [Task Scheduler],described, monthly trigger [Task Scheduler],interface, taskschd.imonthlytrigger, taskschd/IMonthlyTrigger
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: taskschd.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IMonthlyTrigger
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMonthlyTrigger interface


## -description


Represents a trigger that starts a job based on a monthly schedule.  For example, the task starts on specific days of specific months.


## -remarks



The time of day that the task is started is set by the <a href="https://msdn.microsoft.com/749101ae-3db6-44ec-9113-95282c86c3c0">StartBoundary</a> property.

When reading or writing your own XML for a task, a monthly trigger is specified using the <a href="https://msdn.microsoft.com/3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8">ScheduleByMonth </a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>



<a href="https://msdn.microsoft.com/70780fca-ba97-42b8-bc00-867c2761953c">ITriggerCollection::Create</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

