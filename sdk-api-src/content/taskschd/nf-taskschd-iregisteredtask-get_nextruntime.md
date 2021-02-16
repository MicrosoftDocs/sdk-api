---
UID: NF:taskschd.IRegisteredTask.get_NextRunTime
title: IRegisteredTask::get_NextRunTime (taskschd.h)
description: Gets the time when the registered task is next scheduled to run.
helpviewer_keywords: ["IRegisteredTask interface [Task Scheduler]","NextRunTime property","IRegisteredTask.NextRunTime","IRegisteredTask.get_NextRunTime","IRegisteredTask::NextRunTime","IRegisteredTask::get_NextRunTime","NextRunTime property [Task Scheduler]","NextRunTime property [Task Scheduler]","IRegisteredTask interface","get_NextRunTime","taskschd.iregisteredtask_nextruntime","taskschd/IRegisteredTask::NextRunTime","taskschd/IRegisteredTask::get_NextRunTime"]
old-location: taskschd\iregisteredtask_nextruntime.htm
tech.root: taskschd
ms.assetid: ccaed6d7-4247-4299-9226-77d84d572e3b
ms.date: 12/05/2018
ms.keywords: IRegisteredTask interface [Task Scheduler],NextRunTime property, IRegisteredTask.NextRunTime, IRegisteredTask.get_NextRunTime, IRegisteredTask::NextRunTime, IRegisteredTask::get_NextRunTime, NextRunTime property [Task Scheduler], NextRunTime property [Task Scheduler],IRegisteredTask interface, get_NextRunTime, taskschd.iregisteredtask_nextruntime, taskschd/IRegisteredTask::NextRunTime, taskschd/IRegisteredTask::get_NextRunTime
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
 - IRegisteredTask::get_NextRunTime
 - taskschd/IRegisteredTask::get_NextRunTime
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
 - IRegisteredTask.NextRunTime
 - IRegisteredTask.get_NextRunTime
---

# IRegisteredTask::get_NextRunTime


## -description

Gets the time when the registered task is next scheduled to run.

This property is read-only.

## -parameters

## -remarks

If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>