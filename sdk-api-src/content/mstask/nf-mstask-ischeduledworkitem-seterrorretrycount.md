---
UID: NF:mstask.IScheduledWorkItem.SetErrorRetryCount
title: IScheduledWorkItem::SetErrorRetryCount
author: windows-sdk-content
description: Sets the number of times Task Scheduler will try to run the work item again if an error occurs. This method is not implemented.
old-location: taskschd\ischeduledworkitem_seterrorretrycount.htm
old-project: taskschd
ms.assetid: f2c5bafb-a792-4653-87ab-677daec9b10f
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetErrorRetryCount method, IScheduledWorkItem.SetErrorRetryCount, IScheduledWorkItem::SetErrorRetryCount, SetErrorRetryCount, SetErrorRetryCount method [Task Scheduler], SetErrorRetryCount method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_seterrorretrycount, mstask/IScheduledWorkItem::SetErrorRetryCount, taskschd.ischeduledworkitem_seterrorretrycount
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem.SetErrorRetryCount
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::SetErrorRetryCount


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the number of times Task Scheduler will try to run the <a href="https://msdn.microsoft.com/library/Aa381060(v=VS.85).aspx">work item</a> again if an error occurs. This method is not implemented.


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




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/f9935325-124b-4c21-be9c-e9d48fb69791">IScheduledWorkItem::GetErrorRetryCount</a>
 

 

