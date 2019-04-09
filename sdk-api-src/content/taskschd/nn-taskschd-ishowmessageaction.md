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
---

# IShowMessageAction interface


## -description


<p class="CCE_Message">[This interface is no longer supported.  You can use IExecAction with the Windows scripting <a href="https://msdn.microsoft.com/library/sfw6660x(v=VS.85).aspx">MsgBox function</a> to show a message in the user session.]

Represents an action that shows a message  box when a task is activated.


## -remarks



For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.  To set the task logon type to be interactive, specify <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or  <b>TASK_LOGON_GROUP</b> in the <a href="https://msdn.microsoft.com/cf0a8ad4-f1bb-46a2-ae92-d00e08b8d459">LogonType</a> property of the task principal, or in the <i>logonType</i> parameter of <a href="https://msdn.microsoft.com/743e5bd9-3fb6-4e09-96ed-ca2d74fa0bab">ITaskFolder::RegisterTask</a> or <a href="https://msdn.microsoft.com/a94db861-b24e-476a-810d-2cf3bbfc67d1">ITaskFolder::RegisterTaskDefinition</a>. 

When reading or writing your own XML for a task, a message box action is specified using the <a href="https://msdn.microsoft.com/33c6e437-b993-4b5e-b75a-fb3fda9b24df">ShowMessage</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/8c757459-5d23-4359-8c4f-772ef3bde3fc">Message Box Example (C++)</a>.



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/50d60cf0-642a-43fe-9163-51740e75fa8d">IAction</a>
 

 

