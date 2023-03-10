---
UID: NF:taskschd.IRunningTask.Stop
title: IRunningTask::Stop (taskschd.h)
description: Stops this instance of the task.
helpviewer_keywords: ["IRunningTask interface [Task Scheduler]","Stop method","IRunningTask.Stop","IRunningTask::Stop","Stop","Stop method [Task Scheduler]","Stop method [Task Scheduler]","IRunningTask interface","taskschd.irunningtask_stop","taskschd/IRunningTask::Stop"]
old-location: taskschd\irunningtask_stop.htm
tech.root: taskschd
ms.assetid: 2fdf325f-5652-42b0-99e3-3950dba1ef11
ms.date: 12/05/2018
ms.keywords: IRunningTask interface [Task Scheduler],Stop method, IRunningTask.Stop, IRunningTask::Stop, Stop, Stop method [Task Scheduler], Stop method [Task Scheduler],IRunningTask interface, taskschd.irunningtask_stop, taskschd/IRunningTask::Stop
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRunningTask::Stop
 - taskschd/IRunningTask::Stop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IRunningTask.Stop
---

# IRunningTask::Stop


## -description

Stops this instance of the task.



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

<a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtask">IRunningTask</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
