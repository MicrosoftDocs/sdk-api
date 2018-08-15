---
UID: NE:taskschd._TASK_ACTION_TYPE
title: "_TASK_ACTION_TYPE"
author: windows-sdk-content
description: Defines the type of actions that a task can perform.
old-location: taskschd\task_action_type.htm
old-project: taskschd
ms.assetid: 931ea805-fc73-4717-ab40-c12767930df3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TASK_ACTION_COM_HANDLER, TASK_ACTION_EXEC, TASK_ACTION_SEND_EMAIL, TASK_ACTION_SHOW_MESSAGE, TASK_ACTION_TYPE, TASK_ACTION_TYPE enumeration [Task Scheduler], _TASK_ACTION_TYPE, taskschd.actiontype, taskschd.task_action_type, taskschd/TASK_ACTION_COM_HANDLER, taskschd/TASK_ACTION_EXEC, taskschd/TASK_ACTION_SEND_EMAIL, taskschd/TASK_ACTION_SHOW_MESSAGE, taskschd/TASK_ACTION_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: taskschd.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TASK_ACTION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - taskschd.h
api_name:
 - TASK_ACTION_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/50d60cf0-642a-43fe-9163-51740e75fa8d">IAction</a>



<a href="https://msdn.microsoft.com/fb5cc2c3-ba86-401a-b51f-b28d1f5be58f">IComHandlerAction</a>



<a href="https://msdn.microsoft.com/2f08fd42-233a-40ee-96d0-f0ac8b25b847">IEmailAction</a>



<a href="https://msdn.microsoft.com/46a4cd60-df23-4109-8a86-b7755a6922dd">IExecAction</a>



<a href="https://msdn.microsoft.com/329232de-6068-4757-b567-3ce4d2c5ba4a">IShowMessageAction</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

