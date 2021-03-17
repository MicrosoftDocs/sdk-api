---
UID: NF:mstask.IScheduledWorkItem.GetComment
title: IScheduledWorkItem::GetComment (mstask.h)
description: Retrieves the comment for the work item.
helpviewer_keywords: ["GetComment","GetComment method [Task Scheduler]","GetComment method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetComment method","IScheduledWorkItem.GetComment","IScheduledWorkItem::GetComment","_msb_ischeduledworkitem_getcomment","mstask/IScheduledWorkItem::GetComment","taskschd.ischeduledworkitem_getcomment"]
old-location: taskschd\ischeduledworkitem_getcomment.htm
tech.root: taskschd
ms.assetid: 49bfd451-8100-40e1-9727-e54c5478b415
ms.date: 12/05/2018
ms.keywords: GetComment, GetComment method [Task Scheduler], GetComment method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetComment method, IScheduledWorkItem.GetComment, IScheduledWorkItem::GetComment, _msb_ischeduledworkitem_getcomment, mstask/IScheduledWorkItem::GetComment, taskschd.ischeduledworkitem_getcomment
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
 - IScheduledWorkItem::GetComment
 - mstask/IScheduledWorkItem::GetComment
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
 - IScheduledWorkItem.GetComment
---

# IScheduledWorkItem::GetComment


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the comment for the <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -parameters

### -param ppwszComment [out]

A pointer to a null-terminated string that contains the retrieved comment for the current work item.

## -returns

The 
<b>GetComment</b> method returns one of the following values.

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



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setcomment">IScheduledWorkItem::SetComment</a>