---
UID: NF:taskschd.IWeeklyTrigger.put_WeeksInterval
title: IWeeklyTrigger::put_WeeksInterval
author: windows-sdk-content
description: Gets or sets the interval between the weeks in the schedule.
old-location: taskschd\iweeklytrigger_weeksinterval.htm
old-project: taskschd
ms.assetid: 11f2c708-a95b-4b9c-a3a6-9b37b01d2d0b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWeeklyTrigger interface [Task Scheduler],WeeksInterval property, IWeeklyTrigger.WeeksInterval, IWeeklyTrigger.put_WeeksInterval, IWeeklyTrigger::WeeksInterval, IWeeklyTrigger::get_WeeksInterval, IWeeklyTrigger::put_WeeksInterval, WeeksInterval property [Task Scheduler], WeeksInterval property [Task Scheduler],IWeeklyTrigger interface, put_WeeksInterval, taskschd.iweeklytrigger_weeksinterval, taskschd/IWeeklyTrigger::WeeksInterval, taskschd/IWeeklyTrigger::get_WeeksInterval, taskschd/IWeeklyTrigger::put_WeeksInterval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IWeeklyTrigger.WeeksInterval
 - IWeeklyTrigger.get_WeeksInterval
 - IWeeklyTrigger.put_WeeksInterval
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWeeklyTrigger::put_WeeksInterval


## -description


Gets or sets the interval between the weeks in the schedule.

This property is read/write.


## -parameters


## -remarks



An interval of 1 produces a weekly schedule. An interval of 2 produces an every-other week schedule.

When reading or writing your own XML for a task, the interval for a weekly schedule is specified using the <a href="https://msdn.microsoft.com/6cbf1e7e-a695-4012-97fd-fe3360c362c4">WeeksInterval</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/c10b050a-8319-4e21-85aa-0bceb76abaaf">IWeeklyTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

