---
UID: NF:taskschd.IEventTrigger.put_Delay
title: IEventTrigger::put_Delay
author: windows-sdk-content
description: Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.
old-location: taskschd\ieventtrigger_delay.htm
old-project: TaskSchd
ms.assetid: 2731ad62-6384-4c66-b66f-b159a5b15cb1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler],IEventTrigger interface, IEventTrigger interface [Task Scheduler],Delay property, IEventTrigger.Delay, IEventTrigger.put_Delay, IEventTrigger::Delay, IEventTrigger::get_Delay, IEventTrigger::put_Delay, put_Delay, taskschd.ieventtrigger_delay, taskschd/IEventTrigger::Delay, taskschd/IEventTrigger::get_Delay, taskschd/IEventTrigger::put_Delay
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IEventTrigger.Delay
 - IEventTrigger.get_Delay
 - IEventTrigger.put_Delay
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEventTrigger::put_Delay


## -description


Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started. The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes). 

This property is read/write.


## -parameters


## -remarks



When reading or writing your own XML for a task, the event delay is specified using the <a href="https://msdn.microsoft.com/b38bebc7-9818-41f0-a277-cb0e63c28d86">Delay</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/23b7ecb9-d2bb-441a-8c93-126c833f99b9">IEventTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

