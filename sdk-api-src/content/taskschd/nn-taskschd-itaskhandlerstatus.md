---
UID: NN:taskschd.ITaskHandlerStatus
title: ITaskHandlerStatus (taskschd.h)
description: Provides the methods that are used by COM handlers to notify the Task Scheduler about the status of the handler.
old-location: taskschd\itaskhandlerstatus.htm
tech.root: taskschd
ms.assetid: 8b846be3-f05f-4d90-9865-da245c2bfdbf
ms.date: 12/05/2018
ms.keywords: ITaskHandlerStatus, ITaskHandlerStatus interface [Task Scheduler], ITaskHandlerStatus interface [Task Scheduler],described, taskschd.itaskhandlerstatus, taskschd/ITaskHandlerStatus
f1_keywords:
- taskschd/ITaskHandlerStatus
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
- ITaskHandlerStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskHandlerStatus interface


## -description


Provides the methods that are used by COM handlers to notify the Task Scheduler about the status of the handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskHandlerStatus</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskHandlerStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskHandlerStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandlerstatus-taskcompleted">TaskCompleted</a>
</td>
<td align="left" width="63%">
Tells the Task Scheduler that the COM handler is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandlerstatus-updatestatus">UpdateStatus</a>
</td>
<td align="left" width="63%">
Tells the Task Scheduler about the percentage of completion of the COM handler.

</td>
</tr>
</table> 


## -remarks



For information on specifying a COM handler action, see the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction">IComHandlerAction</a> interface.

For information on the required interfaces that must be implemented by the handler, see the  <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskhandler">ITaskHandler</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

