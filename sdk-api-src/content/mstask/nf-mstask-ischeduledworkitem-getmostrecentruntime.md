---
UID: NF:mstask.IScheduledWorkItem.GetMostRecentRunTime
title: IScheduledWorkItem::GetMostRecentRunTime (mstask.h)
description: Retrieves the most recent time the work item began running.
helpviewer_keywords: ["GetMostRecentRunTime","GetMostRecentRunTime method [Task Scheduler]","GetMostRecentRunTime method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetMostRecentRunTime method","IScheduledWorkItem.GetMostRecentRunTime","IScheduledWorkItem::GetMostRecentRunTime","_msb_ischeduledworkitem_getmostrecentruntime","mstask/IScheduledWorkItem::GetMostRecentRunTime","taskschd.ischeduledworkitem_getmostrecentruntime"]
old-location: taskschd\ischeduledworkitem_getmostrecentruntime.htm
tech.root: taskschd
ms.assetid: 38872c60-7d2b-4bfc-b771-98950ab8f40c
ms.date: 12/05/2018
ms.keywords: GetMostRecentRunTime, GetMostRecentRunTime method [Task Scheduler], GetMostRecentRunTime method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetMostRecentRunTime method, IScheduledWorkItem.GetMostRecentRunTime, IScheduledWorkItem::GetMostRecentRunTime, _msb_ischeduledworkitem_getmostrecentruntime, mstask/IScheduledWorkItem::GetMostRecentRunTime, taskschd.ischeduledworkitem_getmostrecentruntime
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
 - IScheduledWorkItem::GetMostRecentRunTime
 - mstask/IScheduledWorkItem::GetMostRecentRunTime
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
 - IScheduledWorkItem.GetMostRecentRunTime
---

# IScheduledWorkItem::GetMostRecentRunTime


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the most recent time the <a href="/windows/desktop/TaskSchd/w">work item</a> began running.

## -parameters

### -param pstLastRun [out]

A pointer to a <b>SYSTEMTIME</b> structure that contains the most recent time the current work item ran.

## -returns

The 
<b>GetMostRecentRunTime</b> method returns one of the following values.

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
<dt><b>SCHED_S_TASK_HAS_NOT_RUN</b></dt>
</dl>
</td>
<td width="60%">
The work item has never run.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getnextruntime">GetNextRunTime</a>



<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>