---
UID: NF:mstask.ITask.SetWorkingDirectory
title: ITask::SetWorkingDirectory (mstask.h)
description: This method sets the working directory for the task.
helpviewer_keywords: ["ITask interface [Task Scheduler]","SetWorkingDirectory method","ITask.SetWorkingDirectory","ITask::SetWorkingDirectory","SetWorkingDirectory","SetWorkingDirectory method [Task Scheduler]","SetWorkingDirectory method [Task Scheduler]","ITask interface","_msb_itask_setworkingdirectory","mstask/ITask::SetWorkingDirectory","taskschd.itask_setworkingdirectory"]
old-location: taskschd\itask_setworkingdirectory.htm
tech.root: taskschd
ms.assetid: df12d899-c254-4bbf-a49f-d89a2fcb0e28
ms.date: 12/05/2018
ms.keywords: ITask interface [Task Scheduler],SetWorkingDirectory method, ITask.SetWorkingDirectory, ITask::SetWorkingDirectory, SetWorkingDirectory, SetWorkingDirectory method [Task Scheduler], SetWorkingDirectory method [Task Scheduler],ITask interface, _msb_itask_setworkingdirectory, mstask/ITask::SetWorkingDirectory, taskschd.itask_setworkingdirectory
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
 - ITask::SetWorkingDirectory
 - mstask/ITask::SetWorkingDirectory
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
 - ITask.SetWorkingDirectory
---

# ITask::SetWorkingDirectory


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method sets the <a href="/windows/desktop/TaskSchd/w">working directory</a> for the <a href="/windows/desktop/TaskSchd/t">task</a>.

## -parameters

### -param pwszWorkingDirectory [in]

A null-terminated string that contains a directory path to the working directory for the task. 




The application starts with this directory as the current working directory. To clear the directory, set <i>pwszWorkingDirectory</i> to L"". If the working directory is set to L"", when the application is run, the current directory will be the directory in which the task scheduler service executable, Mstask.exe, resides.

## -returns

The 
<b>SetWorkingDirectory</b> method returns one of the following values.

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

After setting the working directory of a task, be sure to call <b>IPersistFile::Save</b> to save the modified task object to disk.


#### Examples

For an example of how to set the working directory of a task, see <a href="/windows/desktop/TaskSchd/c-c-code-example-setting-working-directory">C/C++ Code Example: Setting Working Directory</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-itask-getworkingdirectory">GetWorkingDirectory</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>