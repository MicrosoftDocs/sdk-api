---
UID: NF:mstask.IScheduledWorkItem.Terminate
title: IScheduledWorkItem::Terminate (mstask.h)
description: This method ends the execution of the work item.
helpviewer_keywords: ["IScheduledWorkItem interface [Task Scheduler]","Terminate method","IScheduledWorkItem.Terminate","IScheduledWorkItem::Terminate","Terminate","Terminate method [Task Scheduler]","Terminate method [Task Scheduler]","IScheduledWorkItem interface","_msb_ischeduledworkitem_terminate","mstask/IScheduledWorkItem::Terminate","taskschd.ischeduledworkitem_terminate"]
old-location: taskschd\ischeduledworkitem_terminate.htm
tech.root: taskschd
ms.assetid: 8ea2144b-4f51-41db-8eaf-50da83967ea5
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],Terminate method, IScheduledWorkItem.Terminate, IScheduledWorkItem::Terminate, Terminate, Terminate method [Task Scheduler], Terminate method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_terminate, mstask/IScheduledWorkItem::Terminate, taskschd.ischeduledworkitem_terminate
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
 - IScheduledWorkItem::Terminate
 - mstask/IScheduledWorkItem::Terminate
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
 - IScheduledWorkItem.Terminate
---

# IScheduledWorkItem::Terminate


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method ends the execution of the <a href="/windows/desktop/TaskSchd/w">work item</a>.



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

For an example of how to retrieve the task status and terminate a task, see <a href="/windows/desktop/TaskSchd/terminating-a-task-example">Terminating a Task Example</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>
