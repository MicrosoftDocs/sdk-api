---
UID: NF:taskschd.IRegisteredTask.Run
title: IRegisteredTask::Run (taskschd.h)
description: Runs the registered task immediately.
helpviewer_keywords: ["IRegisteredTask interface [Task Scheduler]","Run method","IRegisteredTask.Run","IRegisteredTask::Run","Run","Run method [Task Scheduler]","Run method [Task Scheduler]","IRegisteredTask interface","taskschd.iregisteredtask_run","taskschd/IRegisteredTask::Run"]
old-location: taskschd\iregisteredtask_run.htm
tech.root: taskschd
ms.assetid: 6b237ddd-e4e8-47f7-97e7-360e79841acc
ms.date: 12/05/2018
ms.keywords: IRegisteredTask interface [Task Scheduler],Run method, IRegisteredTask.Run, IRegisteredTask::Run, Run, Run method [Task Scheduler], Run method [Task Scheduler],IRegisteredTask interface, taskschd.iregisteredtask_run, taskschd/IRegisteredTask::Run
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
 - IRegisteredTask::Run
 - taskschd/IRegisteredTask::Run
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
 - IRegisteredTask.Run
---

# IRegisteredTask::Run


## -description

Runs the registered task immediately.

## -parameters

### -param params [in]

The parameters used as  values in the task actions. To not specify any parameter values for the task actions, set this parameter to <b>VT_NULL</b> or <b>VT_EMPTY</b>. Otherwise, a single <b>BSTR</b> value or an array of <b>BSTR</b> values can be specified.

The <b>BSTR</b> values that you specify are paired with names and stored as name-value pairs.  If you specify a single <b>BSTR</b> value, then Arg0 will be the name assigned to the value. The value can be used in the task action where the $(Arg0) variable is used in the action properties.

If you pass in values such as "0", "100", and "250" as an array of <b>BSTR</b> values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables that are used in the action properties.

A maximum of 32 <b>BSTR</b> values can be specified.

For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see <a href="/windows/desktop/TaskSchd/task-actions">Task Actions</a>.

### -param ppRunningTask [out, optional]

An <a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtask">IRunningTask</a> interface that  defines the new instance of the task. 

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtask">IRunningTask</a> interface pointer.  Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method will return without error, but the task will not run if the <a href="/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart">AllowDemandStart</a> property of ITaskSettings is set to false for the task.

The <b>IRegisteredTask::Run</b> function is equivalent to the <a href="/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex">IRegisteredTask::RunEx</a> function with the flags parameter equal to 0 and the user parameter equal to <b>NULL</b>.

If <b>IRegisteredTask::Run</b> is invoked from a disabled task, it will return SCHED_E_TASK_DISABLED.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>