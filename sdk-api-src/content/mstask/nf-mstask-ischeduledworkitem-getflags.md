---
UID: NF:mstask.IScheduledWorkItem.GetFlags
title: IScheduledWorkItem::GetFlags
author: windows-driver-content
description: Retrieves the flags that modify the behavior of any type of work item.
old-location: taskschd\ischeduledworkitem_getflags.htm
old-project: TaskSchd
ms.assetid: 0fe3c184-2689-44de-b60f-92d31eaa5285
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetFlags, GetFlags method [Task Scheduler], GetFlags method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetFlags method, IScheduledWorkItem.GetFlags, IScheduledWorkItem::GetFlags, _msb_ischeduledworkitem_getflags, mstask/IScheduledWorkItem::GetFlags, taskschd.ischeduledworkitem_getflags
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mstask.dll
api_name:
-	IScheduledWorkItem.GetFlags
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IScheduledWorkItem::GetFlags


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the flags that modify the behavior of any type of <a href="w.htm">work item</a>.


## -parameters




### -param pdwFlags [out]

A pointer to a <b>DWORD</b> that contains the flags for the work item. For a list of these flags, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>.


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
<a href="https://msdn.microsoft.com/fd919375-c903-45eb-a8f4-45baf5b42203">ITask::GetTaskFlags</a> is used only to get flags used by scheduled tasks.




## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/640ba3c7-ed9d-4c4c-82fd-34fc777172c2">IScheduledWorkItem::SetFlags</a>



<a href="https://msdn.microsoft.com/fd919375-c903-45eb-a8f4-45baf5b42203">ITask::GetTaskFlags</a>
 

 

