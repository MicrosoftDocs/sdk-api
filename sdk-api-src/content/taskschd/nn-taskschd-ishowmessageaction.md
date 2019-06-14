---
UID: NN:taskschd.IShowMessageAction
title: IShowMessageAction (taskschd.h)
author: windows-sdk-content
description: Represents an action that shows a message box when a task is activated.
old-location: taskschd\ishowmessageaction.htm
tech.root: taskschd
ms.assetid: 329232de-6068-4757-b567-3ce4d2c5ba4a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShowMessageAction, IShowMessageAction interface [Task Scheduler], IShowMessageAction interface [Task Scheduler],described, taskschd.ishowmessageaction, taskschd/IShowMessageAction
ms.topic: interface
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
 - IShowMessageAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShowMessageAction interface


## -description


<p class="CCE_Message">[This interface is no longer supported.  You can use IExecAction with the Windows scripting <a href="https://docs.microsoft.com/previous-versions//sfw6660x(v=vs.85)">MsgBox function</a> to show a message in the user session.]

Represents an action that shows a message  box when a task is activated.


## -remarks



For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.  To set the task logon type to be interactive, specify <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or  <b>TASK_LOGON_GROUP</b> in the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype">LogonType</a> property of the task principal, or in the <i>logonType</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask">ITaskFolder::RegisterTask</a> or <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition">ITaskFolder::RegisterTaskDefinition</a>. 

When reading or writing your own XML for a task, a message box action is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-showmessage-actiongroup-element">ShowMessage</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://docs.microsoft.com/previous-versions//aa381915(v=vs.85)">Message Box Example (C++)</a>.



<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a>
 

 

