---
UID: NF:mstask.ITask.GetApplicationName
title: ITask::GetApplicationName (mstask.h)
description: This method retrieves the name of the application that the task is associated with.
helpviewer_keywords: ["GetApplicationName","GetApplicationName method [Task Scheduler]","GetApplicationName method [Task Scheduler]","ITask interface","ITask interface [Task Scheduler]","GetApplicationName method","ITask.GetApplicationName","ITask::GetApplicationName","_msb_itask_getapplicationname","mstask/ITask::GetApplicationName","taskschd.itask_getapplicationname"]
old-location: taskschd\itask_getapplicationname.htm
tech.root: taskschd
ms.assetid: 79a8c324-1191-412b-be2b-eb5935337925
ms.date: 12/05/2018
ms.keywords: GetApplicationName, GetApplicationName method [Task Scheduler], GetApplicationName method [Task Scheduler],ITask interface, ITask interface [Task Scheduler],GetApplicationName method, ITask.GetApplicationName, ITask::GetApplicationName, _msb_itask_getapplicationname, mstask/ITask::GetApplicationName, taskschd.itask_getapplicationname
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
 - ITask::GetApplicationName
 - mstask/ITask::GetApplicationName
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
 - ITask.GetApplicationName
---

# ITask::GetApplicationName


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method retrieves the name of the application that the <a href="/windows/desktop/TaskSchd/t">task</a> is associated with.

## -parameters

### -param ppwszApplicationName [out]

A pointer to a null-terminated string that contains the name of the application the current task is associated with. After processing this name, call <b>CoTaskMemFree</b> to free resources.

## -returns

The 
<b>GetApplicationName</b> method returns one of the following values.

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



<a href="/windows/desktop/api/mstask/nf-mstask-itask-setapplicationname">ITask::SetApplicationName</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itask-setparameters">SetParameters</a>