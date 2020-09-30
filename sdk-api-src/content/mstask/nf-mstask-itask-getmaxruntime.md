---
UID: NF:mstask.ITask.GetMaxRunTime
title: ITask::GetMaxRunTime (mstask.h)
description: This method retrieves the maximum length of time, in milliseconds, the task can run before terminating.
helpviewer_keywords: ["GetMaxRunTime","GetMaxRunTime method [Task Scheduler]","GetMaxRunTime method [Task Scheduler]","ITask interface","ITask interface [Task Scheduler]","GetMaxRunTime method","ITask.GetMaxRunTime","ITask::GetMaxRunTime","_msb_itask_getmaxruntime","mstask/ITask::GetMaxRunTime","taskschd.itask_getmaxruntime"]
old-location: taskschd\itask_getmaxruntime.htm
tech.root: taskschd
ms.assetid: a9f27929-d304-4696-bb36-0c0a34c71388
ms.date: 12/05/2018
ms.keywords: GetMaxRunTime, GetMaxRunTime method [Task Scheduler], GetMaxRunTime method [Task Scheduler],ITask interface, ITask interface [Task Scheduler],GetMaxRunTime method, ITask.GetMaxRunTime, ITask::GetMaxRunTime, _msb_itask_getmaxruntime, mstask/ITask::GetMaxRunTime, taskschd.itask_getmaxruntime
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
 - ITask::GetMaxRunTime
 - mstask/ITask::GetMaxRunTime
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
 - ITask.GetMaxRunTime
---

# ITask::GetMaxRunTime


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method retrieves the maximum length of time, in milliseconds, the <a href="/windows/desktop/TaskSchd/t">task</a> can run before terminating.

## -parameters

### -param pdwMaxRunTimeMS [out]

A pointer to a <b>DWORD</b> that contains the maximum run time of the current task. 




If the maximum run time is reached during the execution of a task, the Task Scheduler first sends a WM_CLOSE message to the associated application. If the application does not  exit within three minutes, <b>TerminateProcess</b> is run.

## -returns

The 
<b>GetMaxRunTime</b> method returns one of the following values.

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



<a href="/windows/desktop/api/mstask/nf-mstask-itask-setmaxruntime">SetMaxRunTime</a>