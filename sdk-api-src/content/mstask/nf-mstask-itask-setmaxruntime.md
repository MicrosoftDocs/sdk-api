---
UID: NF:mstask.ITask.SetMaxRunTime
title: ITask::SetMaxRunTime (mstask.h)
description: This method sets the maximum time the task can run, in milliseconds, before terminating.
helpviewer_keywords: ["ITask interface [Task Scheduler]","SetMaxRunTime method","ITask.SetMaxRunTime","ITask::SetMaxRunTime","SetMaxRunTime","SetMaxRunTime method [Task Scheduler]","SetMaxRunTime method [Task Scheduler]","ITask interface","_msb_itask_setmaxruntime","mstask/ITask::SetMaxRunTime","taskschd.itask_setmaxruntime"]
old-location: taskschd\itask_setmaxruntime.htm
tech.root: taskschd
ms.assetid: fb9012c6-be41-4ec6-bb1a-73bd7896738f
ms.date: 12/05/2018
ms.keywords: ITask interface [Task Scheduler],SetMaxRunTime method, ITask.SetMaxRunTime, ITask::SetMaxRunTime, SetMaxRunTime, SetMaxRunTime method [Task Scheduler], SetMaxRunTime method [Task Scheduler],ITask interface, _msb_itask_setmaxruntime, mstask/ITask::SetMaxRunTime, taskschd.itask_setmaxruntime
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
 - ITask::SetMaxRunTime
 - mstask/ITask::SetMaxRunTime
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
 - ITask.SetMaxRunTime
---

# ITask::SetMaxRunTime


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method sets the maximum time the <a href="/windows/desktop/TaskSchd/t">task</a> can run, in milliseconds, before terminating.

## -parameters

### -param dwMaxRunTimeMS [in]

A <b>DWORD</b> value that specifies the maximum run time (in milliseconds), for the task. This parameter may be set to INFINITE to specify an unlimited time.

## -returns

The 
<b>SetMaxRunTime</b> method returns one of the following values.

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

When the maximum run time is exceeded, the Task Scheduler attempts to terminate the application associated with the task. If a WM_CLOSE message cannot be sent (for example, the application has no windows) or the application has not exited within three minutes of the receiving WM_CLOSE, the Task Scheduler terminates the application using <b>TerminateProcess</b>.

After setting the maximum run time, be sure to call <b>IPersistFile::Save</b> to save the modified task object to disk.


#### Examples

For an example of how to set the maximum run time, see <a href="/windows/desktop/TaskSchd/c-c-code-example-setting-maxruntime">C/C++ Code Example: Setting MaxRunTime</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-itask-getmaxruntime">IGetMaxRunTime</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>