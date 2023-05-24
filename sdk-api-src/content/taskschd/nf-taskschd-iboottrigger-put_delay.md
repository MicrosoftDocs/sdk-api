---
UID: NF:taskschd.IBootTrigger.put_Delay
title: IBootTrigger::put_Delay (taskschd.h)
description: Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started. (Put)
helpviewer_keywords: ["Delay property [Task Scheduler]","Delay property [Task Scheduler]","IBootTrigger interface","IBootTrigger interface [Task Scheduler]","Delay property","IBootTrigger.Delay","IBootTrigger.put_Delay","IBootTrigger::Delay","IBootTrigger::get_Delay","IBootTrigger::put_Delay","put_Delay","taskschd.iboottrigger_delay","taskschd/IBootTrigger::Delay","taskschd/IBootTrigger::get_Delay","taskschd/IBootTrigger::put_Delay"]
old-location: taskschd\iboottrigger_delay.htm
tech.root: taskschd
ms.assetid: 32173439-1f9e-4780-8fd9-64237bb71075
ms.date: 12/05/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler],IBootTrigger interface, IBootTrigger interface [Task Scheduler],Delay property, IBootTrigger.Delay, IBootTrigger.put_Delay, IBootTrigger::Delay, IBootTrigger::get_Delay, IBootTrigger::put_Delay, put_Delay, taskschd.iboottrigger_delay, taskschd/IBootTrigger::Delay, taskschd/IBootTrigger::get_Delay, taskschd/IBootTrigger::put_Delay
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
 - IBootTrigger::put_Delay
 - taskschd/IBootTrigger::put_Delay
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
 - IBootTrigger.Delay
 - IBootTrigger.get_Delay
 - IBootTrigger.put_Delay
---

# IBootTrigger::put_Delay


## -description

Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.

This property is read/write.

## -parameters

## -remarks

When reading or writing your own XML for a task, the boot delay is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-delay-boottriggertype-element">Delay</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iboottrigger">IBootTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
