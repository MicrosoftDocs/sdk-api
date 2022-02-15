---
UID: NF:mstask.IScheduledWorkItem.Run
title: IScheduledWorkItem::Run (mstask.h)
description: Sends a request to the Task Scheduler service to run the work item.
helpviewer_keywords: ["IScheduledWorkItem interface [Task Scheduler]","Run method","IScheduledWorkItem.Run","IScheduledWorkItem::Run","Run","Run method [Task Scheduler]","Run method [Task Scheduler]","IScheduledWorkItem interface","_msb_ischeduledworkitem_run","mstask/IScheduledWorkItem::Run","taskschd.ischeduledworkitem_run"]
old-location: taskschd\ischeduledworkitem_run.htm
tech.root: taskschd
ms.assetid: f533fcf6-8ece-442f-b6d5-3702321db9e9
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],Run method, IScheduledWorkItem.Run, IScheduledWorkItem::Run, Run, Run method [Task Scheduler], Run method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_run, mstask/IScheduledWorkItem::Run, taskschd.ischeduledworkitem_run
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
 - IScheduledWorkItem::Run
 - mstask/IScheduledWorkItem::Run
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
 - IScheduledWorkItem.Run
---

# IScheduledWorkItem::Run


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sends a request to the Task Scheduler service to run the <a href="/windows/desktop/TaskSchd/w">work item</a>.



## -returns

The 
<b>Run</b> method returns one of the following values.

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

<b>Run</b> is an asynchronous operation. A return code of S_OK means that the request to run the work item has been made; it does not mean that the work item has started running. There may be a delay of a few seconds after 
<b>Run</b> returns before the work item actually starts running.

To determine whether the work item is running, call 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getstatus">IScheduledWorkItem::GetStatus</a>.


#### Examples

For an example of how to start a task, see <a href="/windows/desktop/TaskSchd/starting-a-task-example">Starting a Task Example</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getstatus">IScheduledWorkItem::GetStatus</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>
