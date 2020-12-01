---
UID: NF:mstask.ITask.GetWorkingDirectory
title: ITask::GetWorkingDirectory (mstask.h)
description: This method retrieves the task'sworking directory.
helpviewer_keywords: ["GetWorkingDirectory","GetWorkingDirectory method [Task Scheduler]","GetWorkingDirectory method [Task Scheduler]","ITask interface","ITask interface [Task Scheduler]","GetWorkingDirectory method","ITask.GetWorkingDirectory","ITask::GetWorkingDirectory","_msb_itask_getworkingdirectory","mstask/ITask::GetWorkingDirectory","taskschd.itask_getworkingdirectory"]
old-location: taskschd\itask_getworkingdirectory.htm
tech.root: taskschd
ms.assetid: 737259f6-63d3-43f1-83a7-a10c95aff0e1
ms.date: 12/05/2018
ms.keywords: GetWorkingDirectory, GetWorkingDirectory method [Task Scheduler], GetWorkingDirectory method [Task Scheduler],ITask interface, ITask interface [Task Scheduler],GetWorkingDirectory method, ITask.GetWorkingDirectory, ITask::GetWorkingDirectory, _msb_itask_getworkingdirectory, mstask/ITask::GetWorkingDirectory, taskschd.itask_getworkingdirectory
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
 - ITask::GetWorkingDirectory
 - mstask/ITask::GetWorkingDirectory
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
 - ITask.GetWorkingDirectory
---

# ITask::GetWorkingDirectory


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method retrieves the <a href="/windows/desktop/TaskSchd/t">task's</a><a href="/windows/desktop/TaskSchd/w">working directory</a>.

## -parameters

### -param ppwszWorkingDirectory [in]

A pointer to a null-terminated string that contains the task's working directory. The application that invokes 
<b>GetWorkingDirectory</b> is responsible for freeing this string using the <b>CoTaskMemFree</b> function.

## -returns

The 
<b>GetWorkingDirectory</b> method returns one of the following values.

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



<a href="/windows/desktop/api/mstask/nf-mstask-itask-setworkingdirectory">SetWorkingDirectory</a>