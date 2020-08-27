---
UID: NN:taskschd.IAction
title: IAction (taskschd.h)
description: Provides the common properties inherited by all action objects.
helpviewer_keywords: ["IAction","IAction interface [Task Scheduler]","IAction interface [Task Scheduler]","described","taskschd.iaction","taskschd/IAction"]
old-location: taskschd\iaction.htm
tech.root: taskschd
ms.assetid: 50d60cf0-642a-43fe-9163-51740e75fa8d
ms.date: 12/05/2018
ms.keywords: IAction, IAction interface [Task Scheduler], IAction interface [Task Scheduler],described, taskschd.iaction, taskschd/IAction
f1_keywords:
- taskschd/IAction
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
- IAction
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAction interface


## -description


Provides the common properties inherited by all action objects. An action object is created by the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create">IActionCollection::Create</a> method.


## -remarks



For more information about how actions and tasks work together, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-actions">Task Actions</a>. The following table contains the interfaces that represent the actions  that can be performed:<table>
<tr>
<th>API</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction">IComHandlerAction</a>
</td>
<td>Represents an action that fires a handler.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iexecaction">IExecAction</a>
</td>
<td>Represents an action that executes a command-line operation.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iemailaction">IEmailAction</a>
</td>
<td>Represents an action that sends an email message.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction">IShowMessageAction</a>
</td>
<td>Represents an action that shows a message box.</td>
</tr>
</table>
 



When reading or writing XML, the actions of a task are specified in the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-actions-tasktype-element">Actions</a> element of the Task Scheduler schema.


#### Examples

For more information and a code example  for this interface, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/previous-versions/aa446886(v=vs.85)">Event Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/daily-trigger-example--c---">Daily Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/registration-trigger-example--c---">Registration Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/weekly-trigger-example--c---">Weekly Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/logon-trigger-example--c---">Logon Trigger Example (C++)</a>, or <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/boot-trigger-example--c---">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iactioncollection">IActionCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create">IActionCollection::Create</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

