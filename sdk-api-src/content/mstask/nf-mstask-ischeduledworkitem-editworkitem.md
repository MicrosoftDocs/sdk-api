---
UID: NF:mstask.IScheduledWorkItem.EditWorkItem
title: IScheduledWorkItem::EditWorkItem (mstask.h)
description: Displays the Task, Schedule, and settings property pages for the work item, allowing a user set the properties on those pages.
helpviewer_keywords: ["EditWorkItem","EditWorkItem method [Task Scheduler]","EditWorkItem method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","EditWorkItem method","IScheduledWorkItem.EditWorkItem","IScheduledWorkItem::EditWorkItem","_msb_ischeduledworkitem_editworkitem","mstask/IScheduledWorkItem::EditWorkItem","taskschd.ischeduledworkitem_editworkitem"]
old-location: taskschd\ischeduledworkitem_editworkitem.htm
tech.root: taskschd
ms.assetid: 3b0b335a-4386-4726-8758-ef5944cb5dfe
ms.date: 12/05/2018
ms.keywords: EditWorkItem, EditWorkItem method [Task Scheduler], EditWorkItem method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],EditWorkItem method, IScheduledWorkItem.EditWorkItem, IScheduledWorkItem::EditWorkItem, _msb_ischeduledworkitem_editworkitem, mstask/IScheduledWorkItem::EditWorkItem, taskschd.ischeduledworkitem_editworkitem
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
 - IScheduledWorkItem::EditWorkItem
 - mstask/IScheduledWorkItem::EditWorkItem
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
 - IScheduledWorkItem.EditWorkItem
---

# IScheduledWorkItem::EditWorkItem


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Displays the Task, Schedule, and settings property pages for the <a href="/windows/desktop/TaskSchd/w">work item</a>, allowing a user set the properties on those pages.

## -parameters

### -param hParent [in]

Reserved for future use. Set this parameter to <b>NULL</b>.

### -param dwReserved [in]

Reserved for internal use; this parameter must be set to zero.

## -returns

The 
<b>EditWorkItem</b> method returns one of the following values.

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
<dt><b>STG_E_NOTFILEBASEDSTORAGE</b></dt>
</dl>
</td>
<td width="60%">
The work item object is not persistent.

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