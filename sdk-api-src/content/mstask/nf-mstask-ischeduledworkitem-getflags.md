---
UID: NF:mstask.IScheduledWorkItem.GetFlags
title: IScheduledWorkItem::GetFlags (mstask.h)
description: Retrieves the flags that modify the behavior of any type of work item.
helpviewer_keywords: ["GetFlags","GetFlags method [Task Scheduler]","GetFlags method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetFlags method","IScheduledWorkItem.GetFlags","IScheduledWorkItem::GetFlags","_msb_ischeduledworkitem_getflags","mstask/IScheduledWorkItem::GetFlags","taskschd.ischeduledworkitem_getflags"]
old-location: taskschd\ischeduledworkitem_getflags.htm
tech.root: taskschd
ms.assetid: 0fe3c184-2689-44de-b60f-92d31eaa5285
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Task Scheduler], GetFlags method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetFlags method, IScheduledWorkItem.GetFlags, IScheduledWorkItem::GetFlags, _msb_ischeduledworkitem_getflags, mstask/IScheduledWorkItem::GetFlags, taskschd.ischeduledworkitem_getflags
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
 - IScheduledWorkItem::GetFlags
 - mstask/IScheduledWorkItem::GetFlags
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
 - IScheduledWorkItem.GetFlags
---

# IScheduledWorkItem::GetFlags


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the flags that modify the behavior of any type of <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -parameters

### -param pdwFlags [out]

A pointer to a <b>DWORD</b> that contains the flags for the work item. For a list of these flags, see 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">SetFlags</a>.

## -returns

The 
<b>GetFlags</b> method returns one of the following values.

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

This method is used to get those flags used by any type of scheduled work item. In contrast, 
<a href="/windows/desktop/api/mstask/nf-mstask-itask-gettaskflags">ITask::GetTaskFlags</a> is used only to get flags used by scheduled tasks.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itask-gettaskflags">ITask::GetTaskFlags</a>