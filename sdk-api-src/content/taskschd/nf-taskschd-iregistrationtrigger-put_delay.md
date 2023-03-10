---
UID: NF:taskschd.IRegistrationTrigger.put_Delay
title: IRegistrationTrigger::put_Delay (taskschd.h)
description: Gets or sets the amount of time between when the task is registered and when the task is started. (Put)
helpviewer_keywords: ["Delay property [Task Scheduler]","Delay property [Task Scheduler]","IRegistrationTrigger interface","IRegistrationTrigger interface [Task Scheduler]","Delay property","IRegistrationTrigger.Delay","IRegistrationTrigger.put_Delay","IRegistrationTrigger::Delay","IRegistrationTrigger::get_Delay","IRegistrationTrigger::put_Delay","put_Delay","taskschd.iregistrationtrigger_delay","taskschd/IRegistrationTrigger::Delay","taskschd/IRegistrationTrigger::get_Delay","taskschd/IRegistrationTrigger::put_Delay"]
old-location: taskschd\iregistrationtrigger_delay.htm
tech.root: taskschd
ms.assetid: 9331dd84-a040-4778-baa4-b61981ec6444
ms.date: 12/05/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler],IRegistrationTrigger interface, IRegistrationTrigger interface [Task Scheduler],Delay property, IRegistrationTrigger.Delay, IRegistrationTrigger.put_Delay, IRegistrationTrigger::Delay, IRegistrationTrigger::get_Delay, IRegistrationTrigger::put_Delay, put_Delay, taskschd.iregistrationtrigger_delay, taskschd/IRegistrationTrigger::Delay, taskschd/IRegistrationTrigger::get_Delay, taskschd/IRegistrationTrigger::put_Delay
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRegistrationTrigger::put_Delay
 - taskschd/IRegistrationTrigger::put_Delay
dev_langs:
 - c++
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
---

# IRegistrationTrigger::put_Delay


## -description

Gets or sets the amount of time between when the task is registered and when the task is started. The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, the boot delay is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-delay-registrationtriggertype-element">Delay</a> element of the Task Scheduler schema.

If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during  the delay (before the task runs), then the task will not run and the delay will be lost.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger">IRegistrationTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
