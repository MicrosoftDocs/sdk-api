---
UID: NF:mstask.IEnumWorkItems.Reset
title: IEnumWorkItems::Reset
author: windows-driver-content
description: Resets the enumeration sequence to the beginning.
old-location: taskschd\ienumworkitems_reset.htm
old-project: TaskSchd
ms.assetid: 920ba47b-41cd-462b-9b72-73898a5cd4d0
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IEnumWorkItems interface [Task Scheduler],Reset method, IEnumWorkItems.Reset, IEnumWorkItems::Reset, Reset, Reset method [Task Scheduler], Reset method [Task Scheduler],IEnumWorkItems interface, _msb_ienumworkitems_reset, mstask/IEnumWorkItems::Reset, taskschd.ienumworkitems_reset
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
-	IEnumWorkItems.Reset
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumWorkItems::Reset


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

 Resets the enumeration sequence to the beginning.


## -parameters






## -returns



Returns one of the following values.

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
The enumeration sequence is reset to the beginning of the list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
</table>
 




## -remarks



A call to this method does not guarantee that the same set of tasks will be enumerated after the enumeration sequence is reset. Tasks may have been added to or deleted from the collection while you were enumerating the list.

The 
<a href="https://msdn.microsoft.com/1af162e5-8ba1-4d2e-9451-39c80ac0eecf">IEnumWorkItems</a> interface also provides methods for retrieving sets of tasks, skipping sets of tasks, and making a copy of the current state of the enumeration.




## -see-also




<a href="https://msdn.microsoft.com/1af162e5-8ba1-4d2e-9451-39c80ac0eecf">IEnumWorkItems</a>



<a href="https://msdn.microsoft.com/c42550df-33ad-49cc-ab89-5f952cce2a83">IEnumWorkItems::Clone</a>



<a href="https://msdn.microsoft.com/a606e340-33fb-4a51-acdd-b7428c755ac5">IEnumWorkItems::Next</a>



<a href="https://msdn.microsoft.com/5f4c7c98-a802-4fc3-b88f-bb37826f8199">IEnumWorkItems::Skip</a>
 

 

