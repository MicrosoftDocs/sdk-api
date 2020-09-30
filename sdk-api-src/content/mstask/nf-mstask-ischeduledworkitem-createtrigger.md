---
UID: NF:mstask.IScheduledWorkItem.CreateTrigger
title: IScheduledWorkItem::CreateTrigger (mstask.h)
description: Creates a trigger for the work item.
helpviewer_keywords: ["CreateTrigger","CreateTrigger method [Task Scheduler]","CreateTrigger method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","CreateTrigger method","IScheduledWorkItem.CreateTrigger","IScheduledWorkItem::CreateTrigger","_msb_ischeduledworkitem_createtrigger","mstask/IScheduledWorkItem::CreateTrigger","taskschd.ischeduledworkitem_createtrigger"]
old-location: taskschd\ischeduledworkitem_createtrigger.htm
tech.root: taskschd
ms.assetid: ff8c9c3b-697f-42f0-a5b5-6194e4c89096
ms.date: 12/05/2018
ms.keywords: CreateTrigger, CreateTrigger method [Task Scheduler], CreateTrigger method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],CreateTrigger method, IScheduledWorkItem.CreateTrigger, IScheduledWorkItem::CreateTrigger, _msb_ischeduledworkitem_createtrigger, mstask/IScheduledWorkItem::CreateTrigger, taskschd.ischeduledworkitem_createtrigger
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
 - IScheduledWorkItem::CreateTrigger
 - mstask/IScheduledWorkItem::CreateTrigger
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
 - IScheduledWorkItem.CreateTrigger
---

# IScheduledWorkItem::CreateTrigger


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Creates a trigger for the <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -parameters

### -param piNewTrigger [out]

A pointer to the returned trigger index value of the new trigger. The trigger index for the first trigger associated with a work item is "0". See Remarks for other uses of the trigger index.

### -param ppTrigger [out]

A pointer to a pointer to an 
<a href="/windows/desktop/api/mstask/nn-mstask-itasktrigger">ITaskTrigger</a> interface. Currently, the only supported work items are <a href="/windows/desktop/TaskSchd/t">tasks</a>.

## -returns

The 
<b>CreateTrigger</b> method returns one of the following values.

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

You use the trigger index returned by <i>piNewTrigger</i> when you are either retrieving or  deleting triggers. However, the trigger index is not an identifier. It indicates only the new trigger's position relative to the other current triggers associated with the work item.

To set the criteria for the new trigger, call 
<a href="/windows/desktop/api/mstask/nf-mstask-itasktrigger-settrigger">ITaskTrigger::SetTrigger</a>.

After creating a new trigger for a work item, applications must call the 
<a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a> method to save the new trigger to disk.


#### Examples

For an example of how to set the trigger criteria when creating a new trigger, see <a href="/windows/desktop/TaskSchd/creating-a-new-trigger">Creating a New Trigger</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a>



<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-deletetrigger">IScheduledWorkItem::DeleteTrigger</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-gettrigger">IScheduledWorkItem::GetTrigger</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-gettriggerstring">IScheduledWorkItem::GetTriggerString</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itasktrigger">ITaskTrigger</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itasktrigger-settrigger">ITaskTrigger::SetTrigger</a>