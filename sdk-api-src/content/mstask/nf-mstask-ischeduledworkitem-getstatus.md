---
UID: NF:mstask.IScheduledWorkItem.GetStatus
title: IScheduledWorkItem::GetStatus
author: windows-sdk-content
description: Retrieves the status of the work item.
old-location: taskschd\ischeduledworkitem_getstatus.htm
old-project: TaskSchd
ms.assetid: fb0bc52c-ae50-4c14-864d-099f2903adfb
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetStatus, GetStatus method [Task Scheduler], GetStatus method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetStatus method, IScheduledWorkItem.GetStatus, IScheduledWorkItem::GetStatus, _msb_ischeduledworkitem_getstatus, mstask/IScheduledWorkItem::GetStatus, taskschd.ischeduledworkitem_getstatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mstask.dll
api_name:
-	IScheduledWorkItem.GetStatus
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::GetStatus


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the status of the <a href="w.htm">work item</a>.


## -parameters




### -param phrStatus [out]

A pointer to an <b>HRESULT</b> value that contains one of the following values on return. 







#### SCHED_S_TASK_READY

The work item is ready to run at its next scheduled time.



#### SCHED_S_TASK_RUNNING

The work item is currently running.



#### SCHED_S_TASK_NOT_SCHEDULED

One or more of the properties that are needed to run this task on a schedule have not been set.



#### SCHED_S_TASK_HAS_NOT_RUN

The task has not been run. This value is returned whenever the task has not been run, even if the task is ready to be run at the next scheduled time or the task is a recurring task.



#### SCHED_S_TASK_DISABLED

The task will not run at the scheduled times because it has been disabled.



#### SCHED_S_TASK_NO_MORE_RUNS

There are no more runs scheduled for this task.



#### SCHED_S_TASK_NO_VALID_TRIGGERS

Either the task has no triggers or the existing triggers are disabled or not set. 


## -returns



The 
<b>GetStatus</b> method returns one of the following values.

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
The operation was successful. The request was sent. For more information, see Remarks.

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
</table>
 




## -remarks



The methods of the 
<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a> interface are inherited by the 
<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a> interface. Consequently, 
<b>IScheduledWorkItem::GetStatus</b> is typically called through the 
<b>ITask</b> interface.

<b>IScheduledWorkItem::GetStatus</b> does not obtain the status of the task dynamically. <a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a>
should be called to obtain a new <a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a> interface, which is used to get an updated status. For more information, see the example for <a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a>.


#### Examples

For an example of how to retrieve the status of a task, see <a href="https://msdn.microsoft.com/7ad40ac7-2363-481a-87fa-18dcf2d749b3">C/C++ Code Example: Retrieving Task Status</a>.

For an example of how to retrieve  the task status as part of terminating the task, see <a href="https://msdn.microsoft.com/f8401650-e196-4959-8f23-3d649a55f73d">Terminating a Task Example</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>
 

 

