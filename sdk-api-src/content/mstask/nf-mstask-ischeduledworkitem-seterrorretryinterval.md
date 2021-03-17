---
UID: NF:mstask.IScheduledWorkItem.SetErrorRetryInterval
title: IScheduledWorkItem::SetErrorRetryInterval (mstask.h)
description: Sets the time interval, in minutes, between Task Scheduler's attempts to run a work item after an error occurs. This method is not implemented.
helpviewer_keywords: ["IScheduledWorkItem interface [Task Scheduler]","SetErrorRetryInterval method","IScheduledWorkItem.SetErrorRetryInterval","IScheduledWorkItem::SetErrorRetryInterval","SetErrorRetryInterval","SetErrorRetryInterval method [Task Scheduler]","SetErrorRetryInterval method [Task Scheduler]","IScheduledWorkItem interface","_msb_ischeduledworkitem_seterrorretryinterval","mstask/IScheduledWorkItem::SetErrorRetryInterval","taskschd.ischeduledworkitem_seterrorretryinterval"]
old-location: taskschd\ischeduledworkitem_seterrorretryinterval.htm
tech.root: taskschd
ms.assetid: e5923d76-50d0-4d1c-9d80-0b7cbd8ee3d7
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetErrorRetryInterval method, IScheduledWorkItem.SetErrorRetryInterval, IScheduledWorkItem::SetErrorRetryInterval, SetErrorRetryInterval, SetErrorRetryInterval method [Task Scheduler], SetErrorRetryInterval method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_seterrorretryinterval, mstask/IScheduledWorkItem::SetErrorRetryInterval, taskschd.ischeduledworkitem_seterrorretryinterval
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
 - IScheduledWorkItem::SetErrorRetryInterval
 - mstask/IScheduledWorkItem::SetErrorRetryInterval
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
 - IScheduledWorkItem.SetErrorRetryInterval
---

# IScheduledWorkItem::SetErrorRetryInterval


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the time interval, in minutes, between Task Scheduler's attempts to run a <a href="/windows/desktop/TaskSchd/w">work item</a> after an error occurs. This method is not implemented.

## -parameters

### -param wRetryInterval

A value that specifies the interval between error retries for the current work item, in minutes.

## -returns

The 
<b>SetErrorRetryInterval</b> method returns one of the following values.

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
<b>SetErrorRetryInterval</b> to update the error retry interval.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-geterrorretryinterval">IScheduledWorkItem::GetErrorRetryInterval</a>