---
UID: NF:taskschd.ILogonTrigger.get_Delay
title: ILogonTrigger::get_Delay
author: windows-sdk-content
description: Gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.
old-location: taskschd\ilogontrigger_delay.htm
old-project: taskschd
ms.assetid: 643b25fb-b328-48d7-9eb6-aa3e6fabdd70
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler],ILogonTrigger interface, ILogonTrigger interface [Task Scheduler],Delay property, ILogonTrigger.Delay, ILogonTrigger.get_Delay, ILogonTrigger::Delay, ILogonTrigger::get_Delay, ILogonTrigger::put_Delay, get_Delay, taskschd.ilogontrigger_delay, taskschd/ILogonTrigger::Delay, taskschd/ILogonTrigger::get_Delay, taskschd/ILogonTrigger::put_Delay
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
 - ILogonTrigger.Delay
 - ILogonTrigger.get_Delay
 - ILogonTrigger.put_Delay
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ILogonTrigger::get_Delay


## -description


Gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, the logon trigger delay is specified using the <a href="https://msdn.microsoft.com/daab29f7-5d05-4e6d-a0c0-7b83b4d0b941">Delay</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/c0206a18-53f2-4def-8f54-2b175a0579f4">ILogonTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

