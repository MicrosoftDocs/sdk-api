---
UID: NF:mstask.ITaskScheduler.Enum
title: ITaskScheduler::Enum (mstask.h)
description: The Enum method retrieves a pointer to an OLE enumerator object that enumerates the tasks in the current task folder.
helpviewer_keywords: ["Enum","Enum method [Task Scheduler]","Enum method [Task Scheduler]","ITaskScheduler interface","ITaskScheduler interface [Task Scheduler]","Enum method","ITaskScheduler.Enum","ITaskScheduler::Enum","_msb_itaskscheduler_enum","mstask/ITaskScheduler::Enum","taskschd.itaskscheduler_enum"]
old-location: taskschd\itaskscheduler_enum.htm
tech.root: taskschd
ms.assetid: aca750e3-89b0-47f2-a9b9-49fe5db7f234
ms.date: 12/05/2018
ms.keywords: Enum, Enum method [Task Scheduler], Enum method [Task Scheduler],ITaskScheduler interface, ITaskScheduler interface [Task Scheduler],Enum method, ITaskScheduler.Enum, ITaskScheduler::Enum, _msb_itaskscheduler_enum, mstask/ITaskScheduler::Enum, taskschd.itaskscheduler_enum
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
 - ITaskScheduler::Enum
 - mstask/ITaskScheduler::Enum
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
 - ITaskScheduler.Enum
---

# ITaskScheduler::Enum


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>Enum</b> method retrieves a pointer to an OLE enumerator object that enumerates the tasks in the current task folder.

## -parameters

### -param ppEnumWorkItems [out]

A pointer to a pointer to an 
<a href="/windows/desktop/api/mstask/nn-mstask-ienumworkitems">IEnumWorkItems</a> interface. This interface contains the enumeration context of the current task(s).

## -returns

The 
<b>Enum</b> method returns one of the following values.

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

By default, the current folder resides on the local computer. For remote computers, call 
<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-gettargetcomputer">ITaskScheduler::GetTargetComputer</a> and use the name returned by this call. To change the target computer call 
<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-settargetcomputer">ITaskScheduler::SetTargetComputer</a>.


<table>
<tr>
<th>For a complete example of</th>
<th>See</th>
</tr>
<tr>
<td>Using 
<b>Enum</b> to retrieve the task names on the local computer</td>
<td>
<a href="/windows/desktop/TaskSchd/enumerating-tasks-example">Enumerating Tasks Example</a>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ienumworkitems">IEnumWorkItems</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itaskscheduler">ITaskScheduler</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-gettargetcomputer">ITaskScheduler::GetTargetComputer</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-settargetcomputer">ITaskScheduler::SetTargetComputer</a>