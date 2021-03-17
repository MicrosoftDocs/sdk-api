---
UID: NF:mstask.ITaskScheduler.Delete
title: ITaskScheduler::Delete (mstask.h)
description: The Delete method deletes a task.
helpviewer_keywords: ["Delete","Delete method [Task Scheduler]","Delete method [Task Scheduler]","ITaskScheduler interface","ITaskScheduler interface [Task Scheduler]","Delete method","ITaskScheduler.Delete","ITaskScheduler::Delete","_msb_itaskscheduler_delete","mstask/ITaskScheduler::Delete","taskschd.itaskscheduler_delete"]
old-location: taskschd\itaskscheduler_delete.htm
tech.root: taskschd
ms.assetid: 87f21acc-e6e0-4645-84b8-b35a2eb2e80b
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Task Scheduler], Delete method [Task Scheduler],ITaskScheduler interface, ITaskScheduler interface [Task Scheduler],Delete method, ITaskScheduler.Delete, ITaskScheduler::Delete, _msb_itaskscheduler_delete, mstask/ITaskScheduler::Delete, taskschd.itaskscheduler_delete
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
 - ITaskScheduler::Delete
 - mstask/ITaskScheduler::Delete
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
 - ITaskScheduler.Delete
---

# ITaskScheduler::Delete


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>Delete</b> method deletes a task.

## -parameters

### -param pwszName [in]

A null-terminated string that specifies the name of the task to delete.

## -returns

The 
<b>Delete</b> method returns one of the following values.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-itaskscheduler">ITaskScheduler</a>