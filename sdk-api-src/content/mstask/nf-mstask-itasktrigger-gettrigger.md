---
UID: NF:mstask.ITaskTrigger.GetTrigger
title: ITaskTrigger::GetTrigger (mstask.h)
description: The GetTrigger method retrieves the current task trigger.
helpviewer_keywords: ["GetTrigger","GetTrigger method [Task Scheduler]","GetTrigger method [Task Scheduler]","ITaskTrigger interface","ITaskTrigger interface [Task Scheduler]","GetTrigger method","ITaskTrigger.GetTrigger","ITaskTrigger::GetTrigger","_msb_itasktrigger_gettrigger","mstask/ITaskTrigger::GetTrigger","taskschd.itasktrigger_gettrigger"]
old-location: taskschd\itasktrigger_gettrigger.htm
tech.root: taskschd
ms.assetid: d6c9110d-c79e-475d-871b-83dca6577fc5
ms.date: 12/05/2018
ms.keywords: GetTrigger, GetTrigger method [Task Scheduler], GetTrigger method [Task Scheduler],ITaskTrigger interface, ITaskTrigger interface [Task Scheduler],GetTrigger method, ITaskTrigger.GetTrigger, ITaskTrigger::GetTrigger, _msb_itasktrigger_gettrigger, mstask/ITaskTrigger::GetTrigger, taskschd.itasktrigger_gettrigger
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
 - ITaskTrigger::GetTrigger
 - mstask/ITaskTrigger::GetTrigger
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
 - ITaskTrigger.GetTrigger
---

# ITaskTrigger::GetTrigger


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>GetTrigger</b> method retrieves the current task trigger.

## -parameters

### -param pTrigger [out]

A pointer to a 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure that contains the current task trigger. You must set the <b>cbTriggerSize</b> member of the 
<b>TASK_TRIGGER</b> structure to the size of the task trigger structure before passing the structure to this method.

## -returns

The 
<b>GetTrigger</b> method returns one of the following values.

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
The <i>pTrigger</i> parameter is not valid.

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

A scheduled work item can have one or more triggers defined. The times that the work item will run are the union of all the triggers defined for that item.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-itasktrigger">ITaskTrigger</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itasktrigger-settrigger">ITaskTrigger::SetTrigger</a>



<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a>