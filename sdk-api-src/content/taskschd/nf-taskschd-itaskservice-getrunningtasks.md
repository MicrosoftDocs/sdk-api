---
UID: NF:taskschd.ITaskService.GetRunningTasks
title: ITaskService::GetRunningTasks (taskschd.h)
description: Gets a collection of running tasks.
helpviewer_keywords: ["GetRunningTasks","GetRunningTasks method [Task Scheduler]","GetRunningTasks method [Task Scheduler]","ITaskService interface","ITaskService interface [Task Scheduler]","GetRunningTasks method","ITaskService.GetRunningTasks","ITaskService::GetRunningTasks","taskschd.itaskservice_getrunningtasks","taskschd/ITaskService::GetRunningTasks"]
old-location: taskschd\itaskservice_getrunningtasks.htm
tech.root: taskschd
ms.assetid: 6248cf51-acd8-4317-9837-99dcf918e816
ms.date: 12/05/2018
ms.keywords: GetRunningTasks, GetRunningTasks method [Task Scheduler], GetRunningTasks method [Task Scheduler],ITaskService interface, ITaskService interface [Task Scheduler],GetRunningTasks method, ITaskService.GetRunningTasks, ITaskService::GetRunningTasks, taskschd.itaskservice_getrunningtasks, taskschd/ITaskService::GetRunningTasks
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
 - ITaskService::GetRunningTasks
 - taskschd/ITaskService::GetRunningTasks
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
 - ITaskService.GetRunningTasks
---

# ITaskService::GetRunningTasks


## -description

Gets a collection of running tasks.<div class="alert"><b>Note</b>  <b>ITaskService::GetRunningTasks</b> will only return a collection of running tasks that are running at or below a user's security context. For example, for members of the Administrators group, <b>GetRunningTasks</b> will return a collection of all running tasks, but for members of the Users group, <b>GetRunningTasks</b> will only return a collection of tasks running under the Users group security context.</div>
<div> </div>

## -parameters

### -param flags [in]

A value from the <a href="/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags">TASK_ENUM_FLAGS</a> enumeration. Pass in 0 to return a collection of running tasks that are not hidden tasks.

### -param ppRunningTasks [out]

An <a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection">IRunningTaskCollection</a> interface that contains the currently running tasks.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection">IRunningTaskCollection</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

This method can return one of these values.

<table>
<tr>
<th></th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was specified in the method call. Passing a nonzero value to the <i>flags</i> parameter will return <b>E_INVALIDARG</b>.

</td>
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed into the <i>retVal</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ONLY_IF_CONNECTED)</b></dt>
</dl>
</td>
<td width="60%">
The user has not connected to the service.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection">IRunningTaskCollection</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskservice">ITaskService</a>



<a href="/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags">TASK_ENUM_FLAGS</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>