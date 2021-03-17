---
UID: NF:mstask.ITask.SetTaskFlags
title: ITask::SetTaskFlags (mstask.h)
description: This method sets the flags that modify the behavior of a scheduled task.
helpviewer_keywords: ["ITask interface [Task Scheduler]","SetTaskFlags method","ITask.SetTaskFlags","ITask::SetTaskFlags","SetTaskFlags","SetTaskFlags method [Task Scheduler]","SetTaskFlags method [Task Scheduler]","ITask interface","_msb_itask_settaskflags","mstask/ITask::SetTaskFlags","taskschd.itask_settaskflags"]
old-location: taskschd\itask_settaskflags.htm
tech.root: taskschd
ms.assetid: 32231145-241a-46ff-9c49-94f5bf7cc532
ms.date: 12/05/2018
ms.keywords: ITask interface [Task Scheduler],SetTaskFlags method, ITask.SetTaskFlags, ITask::SetTaskFlags, SetTaskFlags, SetTaskFlags method [Task Scheduler], SetTaskFlags method [Task Scheduler],ITask interface, _msb_itask_settaskflags, mstask/ITask::SetTaskFlags, taskschd.itask_settaskflags
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
 - ITask::SetTaskFlags
 - mstask/ITask::SetTaskFlags
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
 - ITask.SetTaskFlags
---

# ITask::SetTaskFlags


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method sets the flags that modify the behavior of a scheduled <a href="/windows/desktop/TaskSchd/t">task</a>.

## -parameters

### -param dwFlags [in]

Currently, there are no flags defined for scheduled tasks.

## -returns

The 
<b>SetTaskFlags</b> method returns one of the following values.

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

## -remarks

Applications must call the <b>IPersistFile::Save</b> method after calling 
<b>SetTaskFlags</b> to update the task flags.

This method is designed to set the flags that only apply to scheduled tasks. In contrast, 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a> is used to set the flags that apply to all types of scheduled work items.

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-itask-gettaskflags">GetTaskFlags</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>