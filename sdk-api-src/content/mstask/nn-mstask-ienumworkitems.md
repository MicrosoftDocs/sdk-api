---
UID: NN:mstask.IEnumWorkItems
title: IEnumWorkItems
author: windows-sdk-content
description: Provides the methods for enumerating the tasks in the Scheduled Tasks folder.
old-location: taskschd\ienumworkitems.htm
old-project: TaskSchd
ms.assetid: 1af162e5-8ba1-4d2e-9451-39c80ac0eecf
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IEnumWorkItems, IEnumWorkItems interface [Task Scheduler], IEnumWorkItems interface [Task Scheduler],described, _msb_ienumworkitems, mstask/IEnumWorkItems, taskschd.ienumworkitems
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
 - IEnumWorkItems
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumWorkItems interface


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for enumerating the tasks in the <a href="s.htm">Scheduled Tasks folder</a>.

<b>IEnumWorkItems</b> is the primary interface of the <a href="e.htm">enumeration object</a>. To create the enumeration, call 
<a href="https://msdn.microsoft.com/aca750e3-89b0-47f2-a9b9-49fe5db7f234">ITaskScheduler::Enum</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumWorkItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumWorkItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumWorkItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration object in the same state as the current enumeration object: the new object points to the same place in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next set of tasks in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips the next set of tasks in the enumeration sequence.

</td>
</tr>
</table> 

