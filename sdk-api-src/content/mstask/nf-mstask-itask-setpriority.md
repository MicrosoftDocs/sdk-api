---
UID: NF:mstask.ITask.SetPriority
title: ITask::SetPriority (mstask.h)
description: This method sets the priority for the task.
helpviewer_keywords: ["ITask interface [Task Scheduler]","SetPriority method","ITask.SetPriority","ITask::SetPriority","SetPriority","SetPriority method [Task Scheduler]","SetPriority method [Task Scheduler]","ITask interface","_msb_itask_setpriority","mstask/ITask::SetPriority","taskschd.itask_setpriority"]
old-location: taskschd\itask_setpriority.htm
tech.root: taskschd
ms.assetid: f72e5fb8-761e-41bd-be64-b886ebc2c1e5
ms.date: 12/05/2018
ms.keywords: ITask interface [Task Scheduler],SetPriority method, ITask.SetPriority, ITask::SetPriority, SetPriority, SetPriority method [Task Scheduler], SetPriority method [Task Scheduler],ITask interface, _msb_itask_setpriority, mstask/ITask::SetPriority, taskschd.itask_setpriority
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
 - ITask::SetPriority
 - mstask/ITask::SetPriority
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
 - ITask.SetPriority
---

# ITask::SetPriority


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method sets the priority for the <a href="/windows/desktop/TaskSchd/t">task</a>.

## -parameters

### -param dwPriority [in]

A <b>DWORD</b> that specifies the priority for the current task. The priority of a task determines the frequency and length of the time slices for a process. This applies only to the Windows Server 2003, Windows XP, and Windows 2000 operating systems. These values are taken from the <b>CreateProcess</b> priority class and can be one of following flags (in descending order of thread scheduling priority): 




<ul>
<li>REALTIME_PRIORITY_CLASS</li>
<li>HIGH_PRIORITY_CLASS</li>
<li>NORMAL_PRIORITY_CLASS</li>
<li>IDLE_PRIORITY_CLASS</li>
</ul>

## -returns

The 
<b>SetPriority</b> method returns one of the following values.

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
</table>

## -remarks

After setting the priority of a task, call <b>IPersistFile::Save</b> to save the modified task object to disk.


#### Examples

For more information and an example of how to set the priority of  a task, see <a href="/windows/desktop/TaskSchd/c-c-code-example-setting-task-priority">C/C++ Code Example: Setting Task Priority</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-itask-getpriority">GetPriority</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>