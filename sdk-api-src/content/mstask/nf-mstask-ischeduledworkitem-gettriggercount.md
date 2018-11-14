---
UID: NF:mstask.IScheduledWorkItem.GetTriggerCount
title: IScheduledWorkItem::GetTriggerCount
author: windows-sdk-content
description: Retrieves the number of triggers for the current work item.
old-location: taskschd\ischeduledworkitem_gettriggercount.htm
tech.root: TaskSchd
ms.assetid: db1c98db-c4c1-45af-baba-097ee8dc6abf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTriggerCount, GetTriggerCount method [Task Scheduler], GetTriggerCount method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetTriggerCount method, IScheduledWorkItem.GetTriggerCount, IScheduledWorkItem::GetTriggerCount, _msb_ischeduledworkitem_gettriggercount, mstask/IScheduledWorkItem::GetTriggerCount, taskschd.ischeduledworkitem_gettriggercount
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
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem.GetTriggerCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
- apiref
: 
- COM
: 
- mstask.h
: 
- IScheduledWorkItem.GetTriggerCount
: 
---

# IScheduledWorkItem::GetTriggerCount


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the number of <a href="t.htm">triggers</a> for the current <a href="w.htm">work item</a>.


## -parameters




### -param pwCount

TBD




#### - plCount [out]

A pointer to a <b>WORD</b> that will contain the number of triggers associated with the work item.


## -returns



The 
<b>GetTriggerCount</b> method returns one of the following values.

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



<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>
 

 

