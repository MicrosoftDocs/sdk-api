---
UID: NF:mstask.IScheduledWorkItem.SetCreator
title: IScheduledWorkItem::SetCreator (mstask.h)
description: Sets the name of the work item's creator.
helpviewer_keywords: ["IScheduledWorkItem interface [Task Scheduler]","SetCreator method","IScheduledWorkItem.SetCreator","IScheduledWorkItem::SetCreator","SetCreator","SetCreator method [Task Scheduler]","SetCreator method [Task Scheduler]","IScheduledWorkItem interface","_msb_ischeduledworkitem_setcreator","mstask/IScheduledWorkItem::SetCreator","taskschd.ischeduledworkitem_setcreator"]
old-location: taskschd\ischeduledworkitem_setcreator.htm
tech.root: taskschd
ms.assetid: e15c6aba-79f7-407f-81d1-b7ec404c68f9
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetCreator method, IScheduledWorkItem.SetCreator, IScheduledWorkItem::SetCreator, SetCreator, SetCreator method [Task Scheduler], SetCreator method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_setcreator, mstask/IScheduledWorkItem::SetCreator, taskschd.ischeduledworkitem_setcreator
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
 - IScheduledWorkItem::SetCreator
 - mstask/IScheduledWorkItem::SetCreator
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
 - IScheduledWorkItem.SetCreator
---

# IScheduledWorkItem::SetCreator


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the name of the <a href="/windows/desktop/TaskSchd/w">work item's</a> creator.

## -parameters

### -param pwszCreator

A null-terminated string that contains the name of the work item's creator.

## -returns

The 
<b>SetCreator</b> method returns one of the following values.

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

Programs must call the <b>IPersistFile::Save</b> method after calling <b>SetCreator</b> to update the creator.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getcreator">IScheduledWorkItem::GetCreator</a>