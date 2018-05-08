---
UID: NF:mstask.IScheduledWorkItem.GetTrigger
title: IScheduledWorkItem::GetTrigger
author: windows-driver-content
description: Retrieves a task trigger.
old-location: taskschd\ischeduledworkitem_gettrigger.htm
old-project: TaskSchd
ms.assetid: f99b342c-9233-43e3-93f1-88586e975608
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetTrigger, GetTrigger method [Task Scheduler], GetTrigger method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetTrigger method, IScheduledWorkItem.GetTrigger, IScheduledWorkItem::GetTrigger, _msb_ischeduledworkitem_gettrigger, mstask/IScheduledWorkItem::GetTrigger, taskschd.ischeduledworkitem_gettrigger
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
-	IScheduledWorkItem.GetTrigger
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IScheduledWorkItem::GetTrigger


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves a task <a href="t.htm">trigger</a>.


## -parameters




### -param iTrigger [in]

The index of the trigger to retrieve.


### -param ppTrigger [out]

A pointer to a pointer to an 
<a href="https://msdn.microsoft.com/990702f4-fb6f-47a7-b538-f6632f831a4e">ITaskTrigger</a> interface for the retrieved trigger.


## -returns



The 
<b>GetTrigger</b> method returns one of the following values.

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




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/990702f4-fb6f-47a7-b538-f6632f831a4e">ITaskTrigger</a>
 

 

