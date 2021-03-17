---
UID: NF:mstask.IScheduledWorkItem.GetErrorRetryInterval
title: IScheduledWorkItem::GetErrorRetryInterval (mstask.h)
description: Retrieves the time interval, in minutes, between Task Scheduler's attempts to run a work item if an error occurs. This method is not implemented.
helpviewer_keywords: ["GetErrorRetryInterval","GetErrorRetryInterval method [Task Scheduler]","GetErrorRetryInterval method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetErrorRetryInterval method","IScheduledWorkItem.GetErrorRetryInterval","IScheduledWorkItem::GetErrorRetryInterval","_msb_ischeduledworkitem_geterrorretryinterval","mstask/IScheduledWorkItem::GetErrorRetryInterval","taskschd.ischeduledworkitem_geterrorretryinterval"]
old-location: taskschd\ischeduledworkitem_geterrorretryinterval.htm
tech.root: taskschd
ms.assetid: e3ace124-cb02-4d4f-9d6c-18d0d99d64bf
ms.date: 12/05/2018
ms.keywords: GetErrorRetryInterval, GetErrorRetryInterval method [Task Scheduler], GetErrorRetryInterval method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetErrorRetryInterval method, IScheduledWorkItem.GetErrorRetryInterval, IScheduledWorkItem::GetErrorRetryInterval, _msb_ischeduledworkitem_geterrorretryinterval, mstask/IScheduledWorkItem::GetErrorRetryInterval, taskschd.ischeduledworkitem_geterrorretryinterval
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
 - IScheduledWorkItem::GetErrorRetryInterval
 - mstask/IScheduledWorkItem::GetErrorRetryInterval
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
 - IScheduledWorkItem.GetErrorRetryInterval
---

# IScheduledWorkItem::GetErrorRetryInterval


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

 Retrieves the time interval, in minutes, between Task Scheduler's attempts to run a work item if an error occurs. This method is not implemented.

## -parameters

### -param pwRetryInterval [out]

A pointer to a <b>WORD</b> value that contains the time interval between retries of the current work item.

## -returns

The 
<b>GetErrorRetryInterval</b> method returns one of the following values.

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

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-seterrorretryinterval">SetErrorRetryInterval</a>