---
UID: NF:taskschd.IRegistrationTrigger.put_Delay
title: IRegistrationTrigger::put_Delay
author: windows-sdk-content
description: Gets or sets the amount of time between when the task is registered and when the task is started.
old-location: taskschd\iregistrationtrigger_delay.htm
tech.root: taskschd
ms.assetid: 9331dd84-a040-4778-baa4-b61981ec6444
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler],IRegistrationTrigger interface, IRegistrationTrigger interface [Task Scheduler],Delay property, IRegistrationTrigger.Delay, IRegistrationTrigger.put_Delay, IRegistrationTrigger::Delay, IRegistrationTrigger::get_Delay, IRegistrationTrigger::put_Delay, put_Delay, taskschd.iregistrationtrigger_delay, taskschd/IRegistrationTrigger::Delay, taskschd/IRegistrationTrigger::get_Delay, taskschd/IRegistrationTrigger::put_Delay
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
 - IRegistrationTrigger.Delay
 - IRegistrationTrigger.get_Delay
 - IRegistrationTrigger.put_Delay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRegistrationTrigger::put_Delay


## -description


Gets or sets the amount of time between when the task is registered and when the task is started. The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, the boot delay is specified using the <a href="https://msdn.microsoft.com/8955d86c-8306-45e7-93cf-eacf50e10075">Delay</a> element of the Task Scheduler schema.

If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during  the delay (before the task runs), then the task will not run and the delay will be lost. 




## -see-also




<a href="https://msdn.microsoft.com/0862f7ac-69d6-4271-8d39-c5bd7038a95e">IRegistrationTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

