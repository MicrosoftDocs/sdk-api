---
UID: NF:taskschd.IRunningTask.Stop
title: IRunningTask::Stop
author: windows-driver-content
description: Stops this instance of the task.
old-location: taskschd\irunningtask_stop.htm
old-project: TaskSchd
ms.assetid: 2fdf325f-5652-42b0-99e3-3950dba1ef11
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IRunningTask interface [Task Scheduler],Stop method, IRunningTask.Stop, IRunningTask::Stop, Stop, Stop method [Task Scheduler], Stop method [Task Scheduler],IRunningTask interface, taskschd.irunningtask_stop, taskschd/IRunningTask::Stop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IRunningTask.Stop
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRunningTask::Stop


## -description


Stops this instance of the task.


## -parameters






## -returns



This method can return one of these values.

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
The task was stopped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have permission to stop the task, the task is disabled, or the task is not allowed to be run on demand.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/71a06a8f-8628-415d-b002-977c0d27f9a4">IRunningTask</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

