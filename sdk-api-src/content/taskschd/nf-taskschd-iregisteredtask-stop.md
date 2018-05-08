---
UID: NF:taskschd.IRegisteredTask.Stop
title: IRegisteredTask::Stop
author: windows-driver-content
description: Stops the registered task immediately.
old-location: taskschd\iregisteredtask_stop.htm
old-project: TaskSchd
ms.assetid: c58d7b15-1044-4d35-a501-b936503ee0fc
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IRegisteredTask interface [Task Scheduler],Stop method, IRegisteredTask.Stop, IRegisteredTask::Stop, Stop, Stop method [Task Scheduler], Stop method [Task Scheduler],IRegisteredTask interface, taskschd.iregisteredtask_stop, taskschd/IRegisteredTask::Stop
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
-	IRegisteredTask.Stop
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRegisteredTask::Stop


## -description


Stops the registered task immediately.


## -parameters




### -param flags [in]

Reserved. Must be zero.


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
All instances of the registered task that user has permissions to stop were stopped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The user cannot successfully stop instances of the task.

</td>
</tr>
</table>
 




## -remarks



The <b>IRegisteredTask::Stop</b> function stops all instances of the task.

System account users can stop a task, users with Administrator group privileges can stop a task, and if a user has rights to execute and read a task, then the user can stop the task. A user can stop the task instances that are running under the same credentials as the user account. In all other cases, the user is denied access to stop the task.




## -see-also




<a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a>
 

 

