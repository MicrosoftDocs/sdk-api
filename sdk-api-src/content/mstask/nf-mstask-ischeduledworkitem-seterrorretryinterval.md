---
UID: NF:mstask.IScheduledWorkItem.SetErrorRetryInterval
title: IScheduledWorkItem::SetErrorRetryInterval
author: windows-sdk-content
description: Sets the time interval, in minutes, between Task Scheduler's attempts to run a work item after an error occurs. This method is not implemented.
old-location: taskschd\ischeduledworkitem_seterrorretryinterval.htm
old-project: TaskSchd
ms.assetid: e5923d76-50d0-4d1c-9d80-0b7cbd8ee3d7
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetErrorRetryInterval method, IScheduledWorkItem.SetErrorRetryInterval, IScheduledWorkItem::SetErrorRetryInterval, SetErrorRetryInterval, SetErrorRetryInterval method [Task Scheduler], SetErrorRetryInterval method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_seterrorretryinterval, mstask/IScheduledWorkItem::SetErrorRetryInterval, taskschd.ischeduledworkitem_seterrorretryinterval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mstask.dll
api_name:
-	IScheduledWorkItem.SetErrorRetryInterval
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::SetErrorRetryInterval


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the time interval, in minutes, between Task Scheduler's attempts to run a <a href="w.htm">work item</a> after an error occurs. This method is not implemented.


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




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/e3ace124-cb02-4d4f-9d6c-18d0d99d64bf">IScheduledWorkItem::GetErrorRetryInterval</a>
 

 

