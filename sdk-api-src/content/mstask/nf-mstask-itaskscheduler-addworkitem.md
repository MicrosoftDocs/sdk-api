---
UID: NF:mstask.ITaskScheduler.AddWorkItem
title: ITaskScheduler::AddWorkItem (mstask.h)
description: The AddWorkItem method adds a task to the schedule of tasks.
helpviewer_keywords: ["AddWorkItem","AddWorkItem method [Task Scheduler]","AddWorkItem method [Task Scheduler]","ITaskScheduler interface","ITaskScheduler interface [Task Scheduler]","AddWorkItem method","ITaskScheduler.AddWorkItem","ITaskScheduler::AddWorkItem","_msb_itaskscheduler_addworkitem","mstask/ITaskScheduler::AddWorkItem","taskschd.itaskscheduler_addworkitem"]
old-location: taskschd\itaskscheduler_addworkitem.htm
tech.root: taskschd
ms.assetid: 5d776e19-c40e-4e0a-8ae1-a14c4f23b442
ms.date: 12/05/2018
ms.keywords: AddWorkItem, AddWorkItem method [Task Scheduler], AddWorkItem method [Task Scheduler],ITaskScheduler interface, ITaskScheduler interface [Task Scheduler],AddWorkItem method, ITaskScheduler.AddWorkItem, ITaskScheduler::AddWorkItem, _msb_itaskscheduler_addworkitem, mstask/ITaskScheduler::AddWorkItem, taskschd.itaskscheduler_addworkitem
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - ITaskScheduler::AddWorkItem
 - mstask/ITaskScheduler::AddWorkItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - ITaskScheduler.AddWorkItem
---

# ITaskScheduler::AddWorkItem


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>AddWorkItem</b> method adds a task to the schedule of tasks.

## -parameters

### -param pwszTaskName [in]

A null-terminated string that specifies the name of the task to add. The task name must conform to Windows NT file-naming conventions, but cannot include backslashes because nesting within the task folder object is not allowed.

### -param pWorkItem [in]

A pointer to the task to add to the schedule.

## -returns

The 
<b>AddWorkItem</b> method returns one of the following values.

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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A task with the specified name already exists. The actual return value is HRESULT_FROM_WIN32(ERROR_FILE_EXISTS).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the operation.

</td>
</tr>
</table>

## -remarks

Task scheduler provides two methods for adding work items: 
<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-newworkitem">NewWorkItem</a> and 
<b>AddWorkItem</b>. Of these methods, each has its specific advantage. 
<b>AddWorkItem</b> prevents naming collisions, but it also requires two disk write operations per call. One write operation is performed when the call to 
<b>AddWorkItem</b> creates an empty work item object on the disk, followed by another write operation when <b>IPersistFile::Save</b> is called.


<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-newworkitem">NewWorkItem</a> does not prevent naming collisions, but it requires only one disk write operation when <b>IPersistFile::Save</b> is called. Although 
<b>NewWorkItem</b> is more efficient with disk write operations, the application runs the risk of having another application create a work item with the same name before the call to <b>IPersistFile::Save</b> is made.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itaskscheduler">ITaskScheduler</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-newworkitem">ITaskScheduler::NewWorkItem</a>