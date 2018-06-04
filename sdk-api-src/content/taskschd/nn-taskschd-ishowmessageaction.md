---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IShowMessageAction interface


## -description


<p class="CCE_Message">[This interface is no longer supported.  You can use IExecAction with the Windows scripting <a href="ae073d50-e4a4-4e23-8e46-0cb1369965e7">MsgBox function</a> to show a message in the user session.]

Represents an action that shows a message  box when a task is activated.


## -remarks



For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.  To set the task logon type to be interactive, specify <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or  <b>TASK_LOGON_GROUP</b> in the <a href="https://msdn.microsoft.com/cf0a8ad4-f1bb-46a2-ae92-d00e08b8d459">LogonType</a> property of the task principal, or in the <i>logonType</i> parameter of <a href="https://msdn.microsoft.com/743e5bd9-3fb6-4e09-96ed-ca2d74fa0bab">ITaskFolder::RegisterTask</a> or <a href="https://msdn.microsoft.com/a94db861-b24e-476a-810d-2cf3bbfc67d1">ITaskFolder::RegisterTaskDefinition</a>. 

When reading or writing your own XML for a task, a message box action is specified using the <a href="https://msdn.microsoft.com/33c6e437-b993-4b5e-b75a-fb3fda9b24df">ShowMessage</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/8c757459-5d23-4359-8c4f-772ef3bde3fc">Message Box Example (C++)</a>.



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538787">IAction</a>
 

 

