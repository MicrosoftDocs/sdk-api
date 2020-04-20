---
UID: NF:mstask.ITask.GetTaskFlags
title: ITask::GetTaskFlags (mstask.h)
description: This method returns the flags that modify the behavior of a task.helpviewer_keywords: ["GetTaskFlags","GetTaskFlags method [Task Scheduler]","GetTaskFlags method [Task Scheduler]","ITask interface","ITask interface [Task Scheduler]","GetTaskFlags method","ITask.GetTaskFlags","ITask::GetTaskFlags","_msb_itask_gettaskflags","mstask/ITask::GetTaskFlags","taskschd.itask_gettaskflags"]
old-location: taskschd\itask_gettaskflags.htm
tech.root: taskschd
ms.assetid: fd919375-c903-45eb-a8f4-45baf5b42203
ms.date: 12/05/2018
ms.keywords: GetTaskFlags, GetTaskFlags method [Task Scheduler], GetTaskFlags method [Task Scheduler],ITask interface, ITask interface [Task Scheduler],GetTaskFlags method, ITask.GetTaskFlags, ITask::GetTaskFlags, _msb_itask_gettaskflags, mstask/ITask::GetTaskFlags, taskschd.itask_gettaskflags
f1_keywords:
- mstask/ITask.GetTaskFlags
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mstask.dll
api_name:
- ITask.GetTaskFlags
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
---

# ITask::GetTaskFlags


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method returns the flags that modify the behavior of a <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/t">task</a>.


## -parameters




### -param pdwFlags [out]

Currently, there are no defined flags for scheduled tasks.


## -returns



The 
<b>GetTaskFlags</b> method returns one of the following values.

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
 

This method is designed to get the flags that only apply to scheduled tasks. In contrast, 
<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getflags">IScheduledWorkItem::GetFlags</a> is used to get the flags that apply to all types of scheduled work items.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getflags">IScheduledWorkItem::GetFlags</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itask-settaskflags">ITask::SetTaskFlags</a>
 

 

