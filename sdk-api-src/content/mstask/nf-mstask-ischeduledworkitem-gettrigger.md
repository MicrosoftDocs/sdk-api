---
UID: NF:mstask.IScheduledWorkItem.GetTrigger
title: IScheduledWorkItem::GetTrigger (mstask.h)
description: Retrieves a task trigger.
helpviewer_keywords: ["GetTrigger","GetTrigger method [Task Scheduler]","GetTrigger method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetTrigger method","IScheduledWorkItem.GetTrigger","IScheduledWorkItem::GetTrigger","_msb_ischeduledworkitem_gettrigger","mstask/IScheduledWorkItem::GetTrigger","taskschd.ischeduledworkitem_gettrigger"]
old-location: taskschd\ischeduledworkitem_gettrigger.htm
tech.root: taskschd
ms.assetid: f99b342c-9233-43e3-93f1-88586e975608
ms.date: 12/05/2018
ms.keywords: GetTrigger, GetTrigger method [Task Scheduler], GetTrigger method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetTrigger method, IScheduledWorkItem.GetTrigger, IScheduledWorkItem::GetTrigger, _msb_ischeduledworkitem_gettrigger, mstask/IScheduledWorkItem::GetTrigger, taskschd.ischeduledworkitem_gettrigger
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
 - IScheduledWorkItem::GetTrigger
 - mstask/IScheduledWorkItem::GetTrigger
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
 - IScheduledWorkItem.GetTrigger
---

# IScheduledWorkItem::GetTrigger


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves a task <a href="/windows/desktop/TaskSchd/t">trigger</a>.

## -parameters

### -param iTrigger [in]

The index of the trigger to retrieve.

### -param ppTrigger [out]

A pointer to a pointer to an 
<a href="/windows/desktop/api/mstask/nn-mstask-itasktrigger">ITaskTrigger</a> interface for the retrieved trigger.

## -returns

The 
<b>GetTrigger</b> method returns one of the following values.

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

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itasktrigger">ITaskTrigger</a>