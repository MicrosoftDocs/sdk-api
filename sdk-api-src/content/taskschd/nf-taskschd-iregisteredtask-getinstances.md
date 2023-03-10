---
UID: NF:taskschd.IRegisteredTask.GetInstances
title: IRegisteredTask::GetInstances (taskschd.h)
description: Returns all instances of the currently running registered task.
helpviewer_keywords: ["GetInstances","GetInstances method [Task Scheduler]","GetInstances method [Task Scheduler]","IRegisteredTask interface","IRegisteredTask interface [Task Scheduler]","GetInstances method","IRegisteredTask.GetInstances","IRegisteredTask::GetInstances","taskschd.iregisteredtask_getinstances","taskschd/IRegisteredTask::GetInstances"]
old-location: taskschd\iregisteredtask_getinstances.htm
tech.root: taskschd
ms.assetid: 4634851e-e868-4915-a7da-32a39f405974
ms.date: 12/05/2018
ms.keywords: GetInstances, GetInstances method [Task Scheduler], GetInstances method [Task Scheduler],IRegisteredTask interface, IRegisteredTask interface [Task Scheduler],GetInstances method, IRegisteredTask.GetInstances, IRegisteredTask::GetInstances, taskschd.iregisteredtask_getinstances, taskschd/IRegisteredTask::GetInstances
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
 - IRegisteredTask::GetInstances
 - taskschd/IRegisteredTask::GetInstances
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
 - IRegisteredTask.GetInstances
---

# IRegisteredTask::GetInstances


## -description

Returns all instances of the currently running registered task.<div class="alert"><b>Note</b>  <b>IRegisteredTask::GetInstances</b> will only return instances of the currently running registered task that are running at or below a user's security context. For example, for members of the Administrators group, <b>GetInstances</b> will return all instances of the currently running registered task, but for members of the Users group, <b>GetInstances</b> will only return instances of the currently running registered task that are running under the Users group security context.</div>
<div> </div>

## -parameters

### -param flags

This parameter is reserved for future use and must be set to 0.

### -param ppRunningTasks [out]

An <a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection">IRunningTaskCollection</a> interface that contains all currently running instances of the task under the user's context.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection">IRunningTaskCollection</a> interface pointer.  Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A non-null flag was passed into the <i>flags</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed into the <i>ppRunningTasks</i> parameter.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection">IRunningTaskCollection</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>