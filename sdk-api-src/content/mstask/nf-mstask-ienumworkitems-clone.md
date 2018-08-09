---
UID: NF:mstask.IEnumWorkItems.Clone
title: IEnumWorkItems::Clone
author: windows-sdk-content
description: Creates a new enumeration object that contains the same enumeration state as the current enumeration.
old-location: taskschd\ienumworkitems_clone.htm
old-project: taskschd
ms.assetid: c42550df-33ad-49cc-ab89-5f952cce2a83
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Clone, Clone method [Task Scheduler], Clone method [Task Scheduler],IEnumWorkItems interface, IEnumWorkItems interface [Task Scheduler],Clone method, IEnumWorkItems.Clone, IEnumWorkItems::Clone, _msb_ienumworkitems_clone, mstask/IEnumWorkItems::Clone, taskschd.ienumworkitems_clone
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
 - IEnumWorkItems.Clone
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumWorkItems::Clone


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

  Creates a new enumeration object that contains the same enumeration state as the current enumeration.

Because the new object points to the same place in the enumeration sequence, a client can use the 
<b>Clone</b> method to record a particular point in the enumeration sequence and return to that point later.


## -parameters




### -param ppEnumWorkItems [out]

A pointer to a pointer to a new 
<a href="https://msdn.microsoft.com/1af162e5-8ba1-4d2e-9451-39c80ac0eecf">IEnumWorkItems</a> interface. This pointer will point to the newly created enumeration. If the method fails, this parameter is undefined.


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
The argument is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
</table>
 




## -remarks



The 
<a href="https://msdn.microsoft.com/1af162e5-8ba1-4d2e-9451-39c80ac0eecf">IEnumWorkItems</a> interface also provides methods for retrieving sets of tasks, skipping sets of tasks, and resetting the enumeration sequence.




## -see-also




<a href="https://msdn.microsoft.com/1af162e5-8ba1-4d2e-9451-39c80ac0eecf">IEnumWorkItems</a>



<a href="https://msdn.microsoft.com/a606e340-33fb-4a51-acdd-b7428c755ac5">IEnumWorkItems::Next</a>



<a href="https://msdn.microsoft.com/920ba47b-41cd-462b-9b72-73898a5cd4d0">IEnumWorkItems::Reset</a>



<a href="https://msdn.microsoft.com/5f4c7c98-a802-4fc3-b88f-bb37826f8199">IEnumWorkItems::Skip</a>
 

 

