---
UID: NF:mstask.IScheduledWorkItem.SetErrorRetryCount
title: IScheduledWorkItem::SetErrorRetryCount (mstask.h)
description: Sets the number of times Task Scheduler will try to run the work item again if an error occurs. This method is not implemented.
helpviewer_keywords: ["IScheduledWorkItem interface [Task Scheduler]","SetErrorRetryCount method","IScheduledWorkItem.SetErrorRetryCount","IScheduledWorkItem::SetErrorRetryCount","SetErrorRetryCount","SetErrorRetryCount method [Task Scheduler]","SetErrorRetryCount method [Task Scheduler]","IScheduledWorkItem interface","_msb_ischeduledworkitem_seterrorretrycount","mstask/IScheduledWorkItem::SetErrorRetryCount","taskschd.ischeduledworkitem_seterrorretrycount"]
old-location: taskschd\ischeduledworkitem_seterrorretrycount.htm
tech.root: taskschd
ms.assetid: f2c5bafb-a792-4653-87ab-677daec9b10f
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetErrorRetryCount method, IScheduledWorkItem.SetErrorRetryCount, IScheduledWorkItem::SetErrorRetryCount, SetErrorRetryCount, SetErrorRetryCount method [Task Scheduler], SetErrorRetryCount method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_seterrorretrycount, mstask/IScheduledWorkItem::SetErrorRetryCount, taskschd.ischeduledworkitem_seterrorretrycount
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
 - IScheduledWorkItem::SetErrorRetryCount
 - mstask/IScheduledWorkItem::SetErrorRetryCount
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
 - IScheduledWorkItem.SetErrorRetryCount
---

# IScheduledWorkItem::SetErrorRetryCount


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the number of times Task Scheduler will try to run the <a href="/windows/desktop/TaskSchd/w">work item</a> again if an error occurs. This method is not implemented.

## -parameters

### -param wRetryCount

A value that specifies the number of error retries for the current work item.

## -returns

The 
<b>SetErrorRetryCount</b> method returns one of the following values.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

## -remarks

Programs must call the <b>IPersistFile::Save</b> method after calling 
<b>SetErrorRetryCount</b> to update the error retry count.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-geterrorretrycount">IScheduledWorkItem::GetErrorRetryCount</a>