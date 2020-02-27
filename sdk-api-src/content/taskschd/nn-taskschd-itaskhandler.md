---
UID: NN:taskschd.ITaskHandler
title: ITaskHandler (taskschd.h)
description: Defines the methods that are called by the Task Scheduler service to manage a COM handler.
old-location: taskschd\itaskhandler.htm
tech.root: taskschd
ms.assetid: ea3100d7-a80b-4487-9786-24124f2d72f1
ms.date: 12/05/2018
ms.keywords: ITaskHandler, ITaskHandler interface [Task Scheduler], ITaskHandler interface [Task Scheduler],described, taskschd.itaskhandler, taskschd/ITaskHandler
f1_keywords:
- taskschd/ITaskHandler
dev_langs:
- c++
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- taskschd.dll
api_name:
- ITaskHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskHandler interface


## -description


Defines the methods that are called by the Task Scheduler service to manage a COM handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandler-pause">Pause</a>
</td>
<td align="left" width="63%">
Called to pause the COM handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandler-resume">Resume</a>
</td>
<td align="left" width="63%">
Called to restart the COM handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandler-start">Start</a>
</td>
<td align="left" width="63%">
Required. Called to start the COM handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandler-stop">Stop</a>
</td>
<td align="left" width="63%">
Required. Called to stop the COM handler.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

