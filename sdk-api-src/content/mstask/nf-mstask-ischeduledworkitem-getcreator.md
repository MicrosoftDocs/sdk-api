---
UID: NF:mstask.IScheduledWorkItem.GetCreator
title: IScheduledWorkItem::GetCreator (mstask.h)
description: Retrieves the name of the creator of the work item.
helpviewer_keywords: ["GetCreator","GetCreator method [Task Scheduler]","GetCreator method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetCreator method","IScheduledWorkItem.GetCreator","IScheduledWorkItem::GetCreator","_msb_ischeduledworkitem_getcreator","mstask/IScheduledWorkItem::GetCreator","taskschd.ischeduledworkitem_getcreator"]
old-location: taskschd\ischeduledworkitem_getcreator.htm
tech.root: taskschd
ms.assetid: 25bbb200-3418-4ca9-87a5-5db537baceee
ms.date: 12/05/2018
ms.keywords: GetCreator, GetCreator method [Task Scheduler], GetCreator method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetCreator method, IScheduledWorkItem.GetCreator, IScheduledWorkItem::GetCreator, _msb_ischeduledworkitem_getcreator, mstask/IScheduledWorkItem::GetCreator, taskschd.ischeduledworkitem_getcreator
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
 - IScheduledWorkItem::GetCreator
 - mstask/IScheduledWorkItem::GetCreator
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
 - IScheduledWorkItem.GetCreator
---

# IScheduledWorkItem::GetCreator


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the name of the creator of the <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -parameters

### -param ppwszCreator [out]

A pointer to a null-terminated string that contains the name of the creator of the current work item. The application that invokes 
<b>GetCreator</b> is responsible for freeing this string using the <b>CoTaskMemFree</b> function.

## -returns

The 
<b>GetCreator</b> method returns one of the following values.

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



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setcreator">IScheduledWorkItem::SetCreator</a>