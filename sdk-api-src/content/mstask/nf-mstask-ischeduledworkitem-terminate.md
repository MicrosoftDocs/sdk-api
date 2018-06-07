---
UID: NF:mstask.IScheduledWorkItem.Terminate
title: IScheduledWorkItem::Terminate
author: windows-sdk-content
description: This method ends the execution of the work item.
old-location: taskschd\ischeduledworkitem_terminate.htm
old-project: TaskSchd
ms.assetid: 8ea2144b-4f51-41db-8eaf-50da83967ea5
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],Terminate method, IScheduledWorkItem.Terminate, IScheduledWorkItem::Terminate, Terminate, Terminate method [Task Scheduler], Terminate method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_terminate, mstask/IScheduledWorkItem::Terminate, taskschd.ischeduledworkitem_terminate
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem.Terminate
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::Terminate


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method ends the execution of the <a href="/windows/desktop/api/mstask/ns-mstask-_monthlydow">work item</a>.


## -parameters






## -returns



The 
<b>Terminate</b> method returns one of the following values.

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



The 
<b>Terminate</b> method operates asynchronously. It does not wait for the task to terminate before returning a return value.

If the WM_CLOSE message cannot be sent (for example, the application has no windows) or the application has not exited within three minutes of the receiving WM_CLOSE, the Task Scheduler terminates the application using <b>TerminateProcess</b>.


#### Examples

For an example of how to retrieve the task status and terminate a task, see <a href="https://msdn.microsoft.com/f8401650-e196-4959-8f23-3d649a55f73d">Terminating a Task Example</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>
 

 

