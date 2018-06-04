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

# _TASK_ACTION_TYPE enumeration


## -description


Defines the type of actions that a task can perform. 


## -enum-fields




### -field TASK_ACTION_EXEC

This action performs a command-line operation. For example, the action can run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.



### -field TASK_ACTION_COM_HANDLER

This action fires a handler. This action can only be used if the task <a href="https://msdn.microsoft.com/04f77d3c-44fa-4091-b99e-af062f067ef9">Compatibility</a> property is set to TASK_COMPATIBILITY_V2.


### -field TASK_ACTION_SEND_EMAIL

This action sends email message. This action can only be used if the task <a href="https://msdn.microsoft.com/04f77d3c-44fa-4091-b99e-af062f067ef9">Compatibility</a> property is set to TASK_COMPATIBILITY_V2.


### -field TASK_ACTION_SHOW_MESSAGE

This action shows a message box. This action can only be used if the task <a href="https://msdn.microsoft.com/04f77d3c-44fa-4091-b99e-af062f067ef9">Compatibility</a> property is set to TASK_COMPATIBILITY_V2.


## -remarks



The action type is defined when the action is created and cannot be changed later. For C++ development, see <a href="https://msdn.microsoft.com/815a000b-ba02-470d-80e6-06ba3c8ea014">IActionCollection::Create</a>. For scripting development, see <a href="https://msdn.microsoft.com/f33542e1-ee49-4696-b2ab-c48a9b5440d4">ActionCollection.Create</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538787">IAction</a>



<a href="https://msdn.microsoft.com/fb5cc2c3-ba86-401a-b51f-b28d1f5be58f">IComHandlerAction</a>



<a href="https://msdn.microsoft.com/2f08fd42-233a-40ee-96d0-f0ac8b25b847">IEmailAction</a>



<a href="https://msdn.microsoft.com/46a4cd60-df23-4109-8a86-b7755a6922dd">IExecAction</a>



<a href="https://msdn.microsoft.com/329232de-6068-4757-b567-3ce4d2c5ba4a">IShowMessageAction</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

