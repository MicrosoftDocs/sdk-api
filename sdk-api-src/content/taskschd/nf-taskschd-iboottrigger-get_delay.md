---
UID: NF:taskschd.IBootTrigger.get_Delay
title: IBootTrigger::get_Delay
author: windows-sdk-content
description: Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.
old-location: taskschd\iboottrigger_delay.htm
old-project: taskschd
ms.assetid: 32173439-1f9e-4780-8fd9-64237bb71075
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler],IBootTrigger interface, IBootTrigger interface [Task Scheduler],Delay property, IBootTrigger.Delay, IBootTrigger.get_Delay, IBootTrigger::Delay, IBootTrigger::get_Delay, IBootTrigger::put_Delay, get_Delay, taskschd.iboottrigger_delay, taskschd/IBootTrigger::Delay, taskschd/IBootTrigger::get_Delay, taskschd/IBootTrigger::put_Delay
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
 - IBootTrigger.Delay
 - IBootTrigger.get_Delay
 - IBootTrigger.put_Delay
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IBootTrigger::get_Delay


## -description


Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.

This property is read/write.


## -parameters


## -remarks



When reading or writing your own XML for a task, the boot delay is specified using the <a href="https://msdn.microsoft.com/2a583069-ad38-43b4-bcf2-f7c9101f1927">Delay</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/8f186ee2-8d74-426c-9173-523a335422c9">IBootTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

