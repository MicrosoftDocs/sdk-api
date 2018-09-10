---
UID: NF:taskschd.IRegisteredTask.get_NextRunTime
title: IRegisteredTask::get_NextRunTime
author: windows-sdk-content
description: Gets the time when the registered task is next scheduled to run.
old-location: taskschd\iregisteredtask_nextruntime.htm
tech.root: TaskSchd
ms.assetid: ccaed6d7-4247-4299-9226-77d84d572e3b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IRegisteredTask interface [Task Scheduler],NextRunTime property, IRegisteredTask.NextRunTime, IRegisteredTask.get_NextRunTime, IRegisteredTask::NextRunTime, IRegisteredTask::get_NextRunTime, NextRunTime property [Task Scheduler], NextRunTime property [Task Scheduler],IRegisteredTask interface, get_NextRunTime, taskschd.iregisteredtask_nextruntime, taskschd/IRegisteredTask::NextRunTime, taskschd/IRegisteredTask::get_NextRunTime
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
 - IRegisteredTask.NextRunTime
 - IRegisteredTask.get_NextRunTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRegisteredTask::get_NextRunTime


## -description


Gets the time when the registered task is next scheduled to run.

This property is read-only.


## -parameters


## -remarks



If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.




## -see-also




<a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

