---
UID: NF:mstask.ITask.SetParameters
title: ITask::SetParameters (mstask.h)
description: This method sets the command-line parameters for the task.
helpviewer_keywords: ["ITask interface [Task Scheduler]","SetParameters method","ITask.SetParameters","ITask::SetParameters","SetParameters","SetParameters method [Task Scheduler]","SetParameters method [Task Scheduler]","ITask interface","_msb_itask_setparameters","mstask/ITask::SetParameters","taskschd.itask_setparameters"]
old-location: taskschd\itask_setparameters.htm
tech.root: taskschd
ms.assetid: 094dcd8f-35aa-4300-b58d-c846bca1c88c
ms.date: 12/05/2018
ms.keywords: ITask interface [Task Scheduler],SetParameters method, ITask.SetParameters, ITask::SetParameters, SetParameters, SetParameters method [Task Scheduler], SetParameters method [Task Scheduler],ITask interface, _msb_itask_setparameters, mstask/ITask::SetParameters, taskschd.itask_setparameters
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
 - ITask::SetParameters
 - mstask/ITask::SetParameters
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
 - ITask.SetParameters
---

# ITask::SetParameters


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method sets the command-line parameters for the <a href="/windows/desktop/TaskSchd/t">task</a>.

## -parameters

### -param pwszParameters [in]

A null-terminated string that contains task parameters. These parameters are passed as command-line arguments to the application the task will run. To clear the command-line parameter property, set <i>pwszParameters</i> to L"".

## -returns

The 
<b>SetParameters</b> method returns one of the following values.

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

If the task has an application associated with it, the task parameters that are set by this method are ignored.

After setting the parameters of the task, be sure to call <b>IPersistFile::Save</b> to save the modified task object to disk.


#### Examples

For an example of how to set parameters, see <a href="/windows/desktop/TaskSchd/c-c-code-example-setting-task-parameters">C/C++ Code Example: Setting Task Parameters</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>