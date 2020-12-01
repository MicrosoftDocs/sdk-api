---
UID: NF:mstask.ITask.SetApplicationName
title: ITask::SetApplicationName (mstask.h)
description: This method assigns a specific application to the current task.
helpviewer_keywords: ["ITask interface [Task Scheduler]","SetApplicationName method","ITask.SetApplicationName","ITask::SetApplicationName","SetApplicationName","SetApplicationName method [Task Scheduler]","SetApplicationName method [Task Scheduler]","ITask interface","_msb_itask_setapplicationname","mstask/ITask::SetApplicationName","taskschd.itask_setapplicationname"]
old-location: taskschd\itask_setapplicationname.htm
tech.root: taskschd
ms.assetid: 0bec25a9-e653-48b5-be41-8f513169fc8c
ms.date: 12/05/2018
ms.keywords: ITask interface [Task Scheduler],SetApplicationName method, ITask.SetApplicationName, ITask::SetApplicationName, SetApplicationName, SetApplicationName method [Task Scheduler], SetApplicationName method [Task Scheduler],ITask interface, _msb_itask_setapplicationname, mstask/ITask::SetApplicationName, taskschd.itask_setapplicationname
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
 - ITask::SetApplicationName
 - mstask/ITask::SetApplicationName
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
 - ITask.SetApplicationName
---

# ITask::SetApplicationName


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method assigns a specific application to the current <a href="/windows/desktop/TaskSchd/t">task</a>.

## -parameters

### -param pwszApplicationName [in]

A null-terminated string  that contains the name of the application that will be associated with the task. Use an empty string to clear the application name.

## -returns

The 
<b>SetApplicationName</b> method returns one of the following values.

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

If you do not specify a path for the application, the Task Scheduler searches the environment path to find the correct path. If the application name specifies a program, the name should use the .exe extension to ensure that the Task Scheduler user interface properly displays the application's icon.

After calling 
<b>SetApplicationName</b>, make sure you call <b>IPersistFile::Save</b> to save the modified task to disk.


#### Examples

For an example of how to set the application name, see <a href="/windows/desktop/TaskSchd/c-c-code-example-setting-application-name">C/C++ Code Example: Setting Application Name</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-itask-getapplicationname">GetApplicationName</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>