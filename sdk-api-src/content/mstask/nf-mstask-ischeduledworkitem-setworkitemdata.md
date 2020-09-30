---
UID: NF:mstask.IScheduledWorkItem.SetWorkItemData
title: IScheduledWorkItem::SetWorkItemData (mstask.h)
description: This method stores application-defined data associated with the work item.
helpviewer_keywords: ["IScheduledWorkItem interface [Task Scheduler]","SetWorkItemData method","IScheduledWorkItem.SetWorkItemData","IScheduledWorkItem::SetWorkItemData","SetWorkItemData","SetWorkItemData method [Task Scheduler]","SetWorkItemData method [Task Scheduler]","IScheduledWorkItem interface","_msb_ischeduledworkitem_setworkitemdata","mstask/IScheduledWorkItem::SetWorkItemData","taskschd.ischeduledworkitem_setworkitemdata"]
old-location: taskschd\ischeduledworkitem_setworkitemdata.htm
tech.root: taskschd
ms.assetid: 9135b37a-d9f8-4bee-a851-9daca6dc733c
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetWorkItemData method, IScheduledWorkItem.SetWorkItemData, IScheduledWorkItem::SetWorkItemData, SetWorkItemData, SetWorkItemData method [Task Scheduler], SetWorkItemData method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_setworkitemdata, mstask/IScheduledWorkItem::SetWorkItemData, taskschd.ischeduledworkitem_setworkitemdata
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
 - IScheduledWorkItem::SetWorkItemData
 - mstask/IScheduledWorkItem::SetWorkItemData
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
 - IScheduledWorkItem.SetWorkItemData
---

# IScheduledWorkItem::SetWorkItemData


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method stores application-defined data associated with the <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -parameters

### -param cbData [in]

The number of bytes in the data buffer. The caller allocates and frees this memory.

### -param rgbData [in]

The data to copy.

## -returns

The 
<b>SetWorkItemData</b> method returns one of the following values.

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

You can retrieve data by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getworkitemdata">IScheduledWorkItem::GetWorkItemData</a>.

Programs must call the <b>IPersistFile::Save</b> method after calling 
<b>SetWorkItemData</b> to update the work item data.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getworkitemdata">IScheduledWorkItem::GetWorkItemData</a>