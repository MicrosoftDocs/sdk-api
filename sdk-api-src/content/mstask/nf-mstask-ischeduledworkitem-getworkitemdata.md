---
UID: NF:mstask.IScheduledWorkItem.GetWorkItemData
title: IScheduledWorkItem::GetWorkItemData (mstask.h)
description: Retrieves application-defined data associated with the work item.
helpviewer_keywords: ["GetWorkItemData","GetWorkItemData method [Task Scheduler]","GetWorkItemData method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetWorkItemData method","IScheduledWorkItem.GetWorkItemData","IScheduledWorkItem::GetWorkItemData","_msb_ischeduledworkitem_getworkitemdata","mstask/IScheduledWorkItem::GetWorkItemData","taskschd.ischeduledworkitem_getworkitemdata"]
old-location: taskschd\ischeduledworkitem_getworkitemdata.htm
tech.root: taskschd
ms.assetid: 1b37c412-80ed-44fb-8b3a-b142a9669080
ms.date: 12/05/2018
ms.keywords: GetWorkItemData, GetWorkItemData method [Task Scheduler], GetWorkItemData method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetWorkItemData method, IScheduledWorkItem.GetWorkItemData, IScheduledWorkItem::GetWorkItemData, _msb_ischeduledworkitem_getworkitemdata, mstask/IScheduledWorkItem::GetWorkItemData, taskschd.ischeduledworkitem_getworkitemdata
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
 - IScheduledWorkItem::GetWorkItemData
 - mstask/IScheduledWorkItem::GetWorkItemData
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
 - IScheduledWorkItem.GetWorkItemData
---

# IScheduledWorkItem::GetWorkItemData


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves application-defined data associated with the <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -parameters

### -param pcbData [out]

A pointer to the number of bytes copied.

### -param prgbData [out]

A pointer to a pointer to a BYTE that contains user-defined data for the current work item. The method that invokes 
<b>GetWorkItemData</b> is responsible for freeing this memory by using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

The 
<b>GetWorkItemData</b> method returns one of the following values.

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

Retrieving the data of a work item does not affect the operation of the work item in any way.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setworkitemdata">SetWorkItemData</a>