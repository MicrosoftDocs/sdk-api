---
UID: NE:taskschd._TASK_ACTION_TYPE
title: TASK_ACTION_TYPE (taskschd.h)
author: windows-sdk-content
description: Defines the type of actions that a task can perform.
old-location: taskschd\task_action_type.htm
tech.root: taskschd
ms.assetid: 931ea805-fc73-4717-ab40-c12767930df3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TASK_ACTION_COM_HANDLER, TASK_ACTION_EXEC, TASK_ACTION_SEND_EMAIL, TASK_ACTION_SHOW_MESSAGE, TASK_ACTION_TYPE, TASK_ACTION_TYPE enumeration [Task Scheduler], taskschd.actiontype, taskschd.task_action_type, taskschd/TASK_ACTION_COM_HANDLER, taskschd/TASK_ACTION_EXEC, taskschd/TASK_ACTION_SEND_EMAIL, taskschd/TASK_ACTION_SHOW_MESSAGE, taskschd/TASK_ACTION_TYPE
ms.topic: enum
f1_keywords: 
 - "taskschd/TASK_ACTION_TYPE"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: TASK_ACTION_TYPE
req.redist: 
ms.custom: 19H1
---

# TASK_ACTION_TYPE enumeration


## -description


Defines the type of actions that a task can perform. 


## -enum-fields




### -field TASK_ACTION_EXEC

This action performs a command-line operation. For example, the action can run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.



### -field TASK_ACTION_COM_HANDLER

This action fires a handler. This action can only be used if the task <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility">Compatibility</a> property is set to TASK_COMPATIBILITY_V2.


### -field TASK_ACTION_SEND_EMAIL

This action sends email message. This action can only be used if the task <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility">Compatibility</a> property is set to TASK_COMPATIBILITY_V2.


### -field TASK_ACTION_SHOW_MESSAGE

This action shows a message box. This action can only be used if the task <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility">Compatibility</a> property is set to TASK_COMPATIBILITY_V2.


## -remarks



The action type is defined when the action is created and cannot be changed later. For C++ development, see <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create">IActionCollection::Create</a>. For scripting development, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/actioncollection-create">ActionCollection.Create</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction">IComHandlerAction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iemailaction">IEmailAction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iexecaction">IExecAction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction">IShowMessageAction</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
 

 

