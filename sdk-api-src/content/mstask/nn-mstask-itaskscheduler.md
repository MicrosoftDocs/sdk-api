---
UID: NN:mstask.ITaskScheduler
title: ITaskScheduler (mstask.h)
description: Provides the methods for scheduling tasks.
helpviewer_keywords: ["ITaskScheduler","ITaskScheduler interface [Task Scheduler]","ITaskScheduler interface [Task Scheduler]","described","_msb_itaskscheduler","mstask/ITaskScheduler","taskschd.itaskscheduler"]
old-location: taskschd\itaskscheduler.htm
tech.root: taskschd
ms.assetid: 70c276e1-a45a-4a7d-aacc-3eb647675098
ms.date: 12/05/2018
ms.keywords: ITaskScheduler, ITaskScheduler interface [Task Scheduler], ITaskScheduler interface [Task Scheduler],described, _msb_itaskscheduler, mstask/ITaskScheduler, taskschd.itaskscheduler
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
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - ITaskScheduler
 - mstask/ITaskScheduler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - ITaskScheduler
---

# ITaskScheduler interface


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for scheduling tasks.

It is the primary interface of the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/t">task scheduler object</a>. To create a task scheduler object, call <b>CoCreateInstance</b>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskScheduler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskScheduler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">Activate</a>
</td>
<td align="left" width="63%">
Returns an active interface to the specified task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-addworkitem">AddWorkItem</a>
</td>
<td align="left" width="63%">
Adds a task to the schedule of tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes a task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-enum">Enum</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an OLE enumerator object that enumerates the tasks in the current task folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-gettargetcomputer">GetTargetComputer</a>
</td>
<td align="left" width="63%">
Returns the name of the computer on which 
<b>ITaskScheduler</b> is currently targeted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-isoftype">IsOfType</a>
</td>
<td align="left" width="63%">
Checks the object type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-newworkitem">NewWorkItem</a>
</td>
<td align="left" width="63%">
Allocates space for a new task and retrieves its address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mstask/nf-mstask-itaskscheduler-settargetcomputer">SetTargetComputer</a>
</td>
<td align="left" width="63%">
Selects the computer that the 
<b>ITaskScheduler</b> interface operates on.

</td>
</tr>
</table>

