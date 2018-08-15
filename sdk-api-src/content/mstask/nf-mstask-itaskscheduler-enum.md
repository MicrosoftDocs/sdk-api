---
UID: NF:mstask.ITaskScheduler.Enum
title: ITaskScheduler::Enum
author: windows-sdk-content
description: The Enum method retrieves a pointer to an OLE enumerator object that enumerates the tasks in the current task folder.
old-location: taskschd\itaskscheduler_enum.htm
old-project: taskschd
ms.assetid: aca750e3-89b0-47f2-a9b9-49fe5db7f234
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Enum, Enum method [Task Scheduler], Enum method [Task Scheduler],ITaskScheduler interface, ITaskScheduler interface [Task Scheduler],Enum method, ITaskScheduler.Enum, ITaskScheduler::Enum, _msb_itaskscheduler_enum, mstask/ITaskScheduler::Enum, taskschd.itaskscheduler_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mstask.h
req.include-header: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
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
 - ITaskScheduler.Enum
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITaskScheduler::Enum


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>Enum</b> method retrieves a pointer to an OLE enumerator object that enumerates the tasks in the current task folder.


## -parameters




### -param ppEnumWorkItems






#### - ppEnumTasks [out]

A pointer to a pointer to an 
<a href="https://msdn.microsoft.com/1af162e5-8ba1-4d2e-9451-39c80ac0eecf">IEnumWorkItems</a> interface. This interface contains the enumeration context of the current task(s).


## -returns



The 
<b>Enum</b> method returns one of the following values.

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



By default, the current folder resides on the local computer. For remote computers, call 
<a href="https://msdn.microsoft.com/c421a739-3290-4698-88e6-5c746baf903d">ITaskScheduler::GetTargetComputer</a> and use the name returned by this call. To change the target computer call 
<a href="https://msdn.microsoft.com/e56d2384-026e-44e0-b6b7-20a41a421e09">ITaskScheduler::SetTargetComputer</a>.


<table>
<tr>
<th>For a complete example of</th>
<th>See</th>
</tr>
<tr>
<td>Using 
<b>Enum</b> to retrieve the task names on the local computer</td>
<td>
<a href="https://msdn.microsoft.com/65a8a8af-f4d8-4948-8dd4-b592f1381bfe">Enumerating Tasks Example</a>
</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/1af162e5-8ba1-4d2e-9451-39c80ac0eecf">IEnumWorkItems</a>



<a href="https://msdn.microsoft.com/70c276e1-a45a-4a7d-aacc-3eb647675098">ITaskScheduler</a>



<a href="https://msdn.microsoft.com/c421a739-3290-4698-88e6-5c746baf903d">ITaskScheduler::GetTargetComputer</a>



<a href="https://msdn.microsoft.com/e56d2384-026e-44e0-b6b7-20a41a421e09">ITaskScheduler::SetTargetComputer</a>
 

 

