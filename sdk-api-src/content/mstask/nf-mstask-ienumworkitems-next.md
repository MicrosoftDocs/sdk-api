---
UID: NF:mstask.IEnumWorkItems.Next
title: IEnumWorkItems::Next
author: windows-sdk-content
description: Retrieves the next specified number of tasks in the enumeration sequence.
old-location: taskschd\ienumworkitems_next.htm
tech.root: taskschd
ms.assetid: a606e340-33fb-4a51-acdd-b7428c755ac5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumWorkItems interface [Task Scheduler],Next method, IEnumWorkItems.Next, IEnumWorkItems::Next, Next, Next method [Task Scheduler], Next method [Task Scheduler],IEnumWorkItems interface, _msb_ienumworkitems_next, mstask/IEnumWorkItems::Next, taskschd.ienumworkitems_next
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
 - IEnumWorkItems.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# IEnumWorkItems::Next


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the next specified number of tasks in the enumeration sequence.

If there are fewer than the requested number of tasks left in the sequence, all the remaining elements are retrieved.


## -parameters




### -param celt [in]

The number of tasks to retrieve.


### -param rgpwszNames [out]

A pointer to an array of pointers (<b>LPWSTR</b>) to <b>null</b>-terminated character strings containing the file names of the tasks returned from the enumeration sequence. These file names are taken from the <a href="s.htm">Scheduled Tasks folder</a> and have the ".job" extension.

After processing the names returned in <i>rgpwszNames</i>, you must first free each character string in the array and then the array itself using <b>CoTaskMemFree</b>.


### -param pceltFetched [out]

A pointer to the number of tasks returned in <i>rgpwszNames</i>. If the <i>celt</i> parameter is 1, this parameter may be <b>NULL</b>.


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
The number of tasks retrieved equals the number requested.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number returned is less than the number requested. (Thus, there are no more tasks to enumerate.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid.

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



The 
<a href="https://msdn.microsoft.com/1af162e5-8ba1-4d2e-9451-39c80ac0eecf">IEnumWorkItems</a> interface also provides methods for resetting the enumeration, skipping tasks, and making a copy of the current state of the enumeration.


#### Examples

For an example of how to use <b>Next</b> to enumerate the tasks in the Scheduled Tasks folder, see <a href="https://msdn.microsoft.com/65a8a8af-f4d8-4948-8dd4-b592f1381bfe">Enumerating Tasks Example</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1af162e5-8ba1-4d2e-9451-39c80ac0eecf">IEnumWorkItems</a>



<a href="https://msdn.microsoft.com/c42550df-33ad-49cc-ab89-5f952cce2a83">IEnumWorkItems::Clone</a>



<a href="https://msdn.microsoft.com/920ba47b-41cd-462b-9b72-73898a5cd4d0">IEnumWorkItems::Reset</a>



<a href="https://msdn.microsoft.com/5f4c7c98-a802-4fc3-b88f-bb37826f8199">IEnumWorkItems::Skip</a>
 

 

