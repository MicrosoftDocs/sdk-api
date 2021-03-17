---
UID: NF:taskschd.IRunningTask.get_State
title: IRunningTask::get_State (taskschd.h)
description: Gets an identifier for the state of the running task.
helpviewer_keywords: ["IRunningTask interface [Task Scheduler]","State property","IRunningTask.State","IRunningTask.get_State","IRunningTask::State","IRunningTask::get_State","State property [Task Scheduler]","State property [Task Scheduler]","IRunningTask interface","TASK_STATE_DISABLED","TASK_STATE_QUEUED","TASK_STATE_READY","TASK_STATE_RUNNING","TASK_STATE_UNKNOWN","get_State","taskschd.irunningtask_state","taskschd/IRunningTask::State","taskschd/IRunningTask::get_State"]
old-location: taskschd\irunningtask_state.htm
tech.root: taskschd
ms.assetid: 50a1d81d-9762-4d1f-801a-b2c54ad9c5bc
ms.date: 12/05/2018
ms.keywords: IRunningTask interface [Task Scheduler],State property, IRunningTask.State, IRunningTask.get_State, IRunningTask::State, IRunningTask::get_State, State property [Task Scheduler], State property [Task Scheduler],IRunningTask interface, TASK_STATE_DISABLED, TASK_STATE_QUEUED, TASK_STATE_READY, TASK_STATE_RUNNING, TASK_STATE_UNKNOWN, get_State, taskschd.irunningtask_state, taskschd/IRunningTask::State, taskschd/IRunningTask::get_State
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
 - IRunningTask::get_State
 - taskschd/IRunningTask::get_State
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
 - IRunningTask.State
 - IRunningTask.get_State
---

# IRunningTask::get_State


## -description

Gets an identifier for the state of the running task.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/taskschd/nf-taskschd-irunningtask-refresh">IRunningTask::Refresh</a> method is called before the property value is returned.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtask">IRunningTask</a>