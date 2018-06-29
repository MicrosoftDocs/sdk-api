---
UID: NN:mstask.ITaskScheduler
title: ITaskScheduler
author: windows-sdk-content
description: Provides the methods for scheduling tasks.
old-location: taskschd\itaskscheduler.htm
old-project: TaskSchd
ms.assetid: 70c276e1-a45a-4a7d-aacc-3eb647675098
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITaskScheduler, ITaskScheduler interface [Task Scheduler], ITaskScheduler interface [Task Scheduler],described, _msb_itaskscheduler, mstask/ITaskScheduler, taskschd.itaskscheduler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITaskScheduler
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITaskScheduler interface


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for scheduling tasks.

It is the primary interface of the <a href="https://msdn.microsoft.com/library/Aa381052(v=VS.85).aspx">task scheduler object</a>. To create a task scheduler object, call <b>CoCreateInstance</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskScheduler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITaskScheduler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskScheduler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">Activate</a>
</td>
<td align="left" width="63%">
Returns an active interface to the specified task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d776e19-c40e-4e0a-8ae1-a14c4f23b442">AddWorkItem</a>
</td>
<td align="left" width="63%">
Adds a task to the schedule of tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87f21acc-e6e0-4645-84b8-b35a2eb2e80b">Delete</a>
</td>
<td align="left" width="63%">
Deletes a task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aca750e3-89b0-47f2-a9b9-49fe5db7f234">Enum</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an OLE enumerator object that enumerates the tasks in the current task folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c421a739-3290-4698-88e6-5c746baf903d">GetTargetComputer</a>
</td>
<td align="left" width="63%">
Returns the name of the computer on which 
<b>ITaskScheduler</b> is currently targeted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d0a474d-398f-4d85-8e58-5dc2b6283086">IsOfType</a>
</td>
<td align="left" width="63%">
Checks the object type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fbd65ae-0b54-4175-bf26-4226b1aabdc1">NewWorkItem</a>
</td>
<td align="left" width="63%">
Allocates space for a new task and retrieves its address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e56d2384-026e-44e0-b6b7-20a41a421e09">SetTargetComputer</a>
</td>
<td align="left" width="63%">
Selects the computer that the 
<b>ITaskScheduler</b> interface operates on.

</td>
</tr>
</table> 

