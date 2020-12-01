---
UID: NF:mstask.IScheduledWorkItem.GetNextRunTime
title: IScheduledWorkItem::GetNextRunTime (mstask.h)
description: Retrieves the next time the work item will run.
helpviewer_keywords: ["GetNextRunTime","GetNextRunTime method [Task Scheduler]","GetNextRunTime method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetNextRunTime method","IScheduledWorkItem.GetNextRunTime","IScheduledWorkItem::GetNextRunTime","_msb_ischeduledworkitem_getnextruntime","mstask/IScheduledWorkItem::GetNextRunTime","taskschd.ischeduledworkitem_getnextruntime"]
old-location: taskschd\ischeduledworkitem_getnextruntime.htm
tech.root: taskschd
ms.assetid: a53700f7-0e2c-413f-b7b3-64aa2e970f11
ms.date: 12/05/2018
ms.keywords: GetNextRunTime, GetNextRunTime method [Task Scheduler], GetNextRunTime method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetNextRunTime method, IScheduledWorkItem.GetNextRunTime, IScheduledWorkItem::GetNextRunTime, _msb_ischeduledworkitem_getnextruntime, mstask/IScheduledWorkItem::GetNextRunTime, taskschd.ischeduledworkitem_getnextruntime
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
 - IScheduledWorkItem::GetNextRunTime
 - mstask/IScheduledWorkItem::GetNextRunTime
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
 - IScheduledWorkItem.GetNextRunTime
---

# IScheduledWorkItem::GetNextRunTime


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the next time the <a href="/windows/desktop/TaskSchd/w">work item</a> will run.

## -parameters

### -param pstNextRun [out]

A pointer to a <b>SYSTEMTIME</b> structure that contains the next time the work item will run.

## -returns

The 
<b>GetNextRunTime</b> method returns one of the following values.

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
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_S_TASK_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The task will not run at the scheduled times because it has been disabled.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>