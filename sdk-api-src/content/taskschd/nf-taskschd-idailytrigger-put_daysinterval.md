---
UID: NF:taskschd.IDailyTrigger.put_DaysInterval
title: IDailyTrigger::put_DaysInterval
author: windows-driver-content
description: Gets or sets the interval between the days in the schedule.
old-location: taskschd\idailytrigger_daysinterval.htm
old-project: TaskSchd
ms.assetid: fde401c7-f0ab-46bd-9b84-bd9f762f2c89
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DaysInterval property [Task Scheduler], DaysInterval property [Task Scheduler],IDailyTrigger interface, IDailyTrigger interface [Task Scheduler],DaysInterval property, IDailyTrigger.DaysInterval, IDailyTrigger.put_DaysInterval, IDailyTrigger::DaysInterval, IDailyTrigger::get_DaysInterval, IDailyTrigger::put_DaysInterval, put_DaysInterval, taskschd.idailytrigger_daysinterval, taskschd/IDailyTrigger::DaysInterval, taskschd/IDailyTrigger::get_DaysInterval, taskschd/IDailyTrigger::put_DaysInterval
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IDailyTrigger.DaysInterval
-	IDailyTrigger.get_DaysInterval
-	IDailyTrigger.put_DaysInterval
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDailyTrigger::put_DaysInterval


## -description


Gets or sets the interval between the days in the schedule.

This property is read/write.


## -parameters


## -remarks



An interval of 1 produces a daily schedule. An interval of 2 produces an every-other day schedule.

When reading or writing your own XML for a task, the interval for a daily schedule is specified using the <a href="https://msdn.microsoft.com/495ea1c0-37eb-4b12-8241-bfc6489e33ed">DaysInterval</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/9980ddb1-9873-46d2-8dea-bfc3fd78bba8">IDailyTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

