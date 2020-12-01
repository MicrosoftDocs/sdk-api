---
UID: NF:mstask.ITask.GetPriority
title: ITask::GetPriority (mstask.h)
description: This method retrieves the priority for the task.
helpviewer_keywords: ["GetPriority","GetPriority method [Task Scheduler]","GetPriority method [Task Scheduler]","ITask interface","ITask interface [Task Scheduler]","GetPriority method","ITask.GetPriority","ITask::GetPriority","_msb_itask_getpriority","mstask/ITask::GetPriority","taskschd.itask_getpriority"]
old-location: taskschd\itask_getpriority.htm
tech.root: taskschd
ms.assetid: 4ace8ab8-e629-4cf9-9bdf-416b2f67c4cd
ms.date: 12/05/2018
ms.keywords: GetPriority, GetPriority method [Task Scheduler], GetPriority method [Task Scheduler],ITask interface, ITask interface [Task Scheduler],GetPriority method, ITask.GetPriority, ITask::GetPriority, _msb_itask_getpriority, mstask/ITask::GetPriority, taskschd.itask_getpriority
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITask::GetPriority
 - mstask/ITask::GetPriority
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
 - ITask.GetPriority
---

# ITask::GetPriority


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method retrieves the priority for the <a href="/windows/desktop/TaskSchd/t">task</a>.

## -parameters

### -param pdwPriority [out]

A pointer to a <b>DWORD</b> that contains the priority for the current task. The priority value determines the frequency and length of the time slices for a process. This applies only to the Windows Server 2003, Windows XP, and Windows 2000 operating systems. It is taken from the CreateProcess priority class and can be one of the following flags (in descending order of thread scheduling priority): 




<ul>
<li>REALTIME_PRIORITY_CLASS</li>
<li>HIGH_PRIORITY_CLASS</li>
<li>NORMAL_PRIORITY_CLASS</li>
<li>IDLE_PRIORITY_CLASS</li>
</ul>

## -returns

The 
<b>GetPriority</b> method returns one of the following values.

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

<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itask-setpriority">SetPriority</a>