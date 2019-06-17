---
UID: NF:taskschd.ILogonTrigger.get_Delay
title: ILogonTrigger::get_Delay (taskschd.h)
author: windows-sdk-content
description: Gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.
old-location: taskschd\ilogontrigger_delay.htm
tech.root: taskschd
ms.assetid: 643b25fb-b328-48d7-9eb6-aa3e6fabdd70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler],ILogonTrigger interface, ILogonTrigger interface [Task Scheduler],Delay property, ILogonTrigger.Delay, ILogonTrigger.get_Delay, ILogonTrigger::Delay, ILogonTrigger::get_Delay, ILogonTrigger::put_Delay, get_Delay, taskschd.ilogontrigger_delay, taskschd/ILogonTrigger::Delay, taskschd/ILogonTrigger::get_Delay, taskschd/ILogonTrigger::put_Delay
ms.topic: method
f1_keywords: ["taskschd/ILogonTrigger.Delay"]
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
 - ILogonTrigger.Delay
 - ILogonTrigger.get_Delay
 - ILogonTrigger.put_Delay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILogonTrigger::get_Delay


## -description


Gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, the logon trigger delay is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-delay-logontriggertype-element">Delay</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger">ILogonTrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

