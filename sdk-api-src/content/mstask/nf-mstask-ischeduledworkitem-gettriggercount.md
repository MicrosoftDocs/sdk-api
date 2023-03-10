---
UID: NF:mstask.IScheduledWorkItem.GetTriggerCount
title: IScheduledWorkItem::GetTriggerCount (mstask.h)
description: Retrieves the number of triggers for the current work item.
helpviewer_keywords: ["GetTriggerCount","GetTriggerCount method [Task Scheduler]","GetTriggerCount method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetTriggerCount method","IScheduledWorkItem.GetTriggerCount","IScheduledWorkItem::GetTriggerCount","_msb_ischeduledworkitem_gettriggercount","mstask/IScheduledWorkItem::GetTriggerCount","taskschd.ischeduledworkitem_gettriggercount"]
old-location: taskschd\ischeduledworkitem_gettriggercount.htm
tech.root: taskschd
ms.assetid: db1c98db-c4c1-45af-baba-097ee8dc6abf
ms.date: 12/05/2018
ms.keywords: GetTriggerCount, GetTriggerCount method [Task Scheduler], GetTriggerCount method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetTriggerCount method, IScheduledWorkItem.GetTriggerCount, IScheduledWorkItem::GetTriggerCount, _msb_ischeduledworkitem_gettriggercount, mstask/IScheduledWorkItem::GetTriggerCount, taskschd.ischeduledworkitem_gettriggercount
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
 - IScheduledWorkItem::GetTriggerCount
 - mstask/IScheduledWorkItem::GetTriggerCount
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
 - IScheduledWorkItem.GetTriggerCount
---

# IScheduledWorkItem::GetTriggerCount


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the number of <a href="/windows/desktop/TaskSchd/t">triggers</a> for the current <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -parameters

### -param pwCount [out]

A pointer to a <b>WORD</b> that will contain the number of triggers associated with the work item.

## -returns

The 
<b>GetTriggerCount</b> method returns one of the following values.

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



<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>