---
UID: NF:mstask.IScheduledWorkItem.GetNextRunTime
title: IScheduledWorkItem::GetNextRunTime method
author: windows-driver-content
description: Retrieves the next time the work item will run.
old-location: taskschd\ischeduledworkitem_getnextruntime.htm
old-project: TaskSchd
ms.assetid: a53700f7-0e2c-413f-b7b3-64aa2e970f11
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetNextRunTime method [Task Scheduler], GetNextRunTime method [Task Scheduler], IScheduledWorkItem interface, GetNextRunTime,IScheduledWorkItem.GetNextRunTime, IScheduledWorkItem, IScheduledWorkItem interface [Task Scheduler], GetNextRunTime method, IScheduledWorkItem::GetNextRunTime, _msb_ischeduledworkitem_getnextruntime, mstask/IScheduledWorkItem::GetNextRunTime, taskschd.ischeduledworkitem_getnextruntime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mstask.dll
api_name:
-	IScheduledWorkItem.GetNextRunTime
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IScheduledWorkItem::GetNextRunTime method


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the next time the <a href="w.htm">work item</a> will run.


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




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>
 

 

