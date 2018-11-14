---
UID: NF:taskschd.IAction.get_Type
title: IAction::get_Type
author: windows-sdk-content
description: Gets the type of action.
old-location: taskschd\iaction_type.htm
tech.root: TaskSchd
ms.assetid: 720aae58-b58c-4948-9e94-94c5a041a2db
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAction interface [Task Scheduler],Type property, IAction.Type, IAction.get_Type, IAction::Type, IAction::get_Type, TASK_ACTION_COM_HANDLER, TASK_ACTION_EXEC, TASK_ACTION_SEND_EMAIL, TASK_ACTION_SHOW_MESSAGE, Type property [Task Scheduler], Type property [Task Scheduler],IAction interface, get_Type, taskschd.iaction_type, taskschd/IAction::Type, taskschd/IAction::get_Type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAction.Type
 - IAction.get_Type
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- taskschd.h
: 
- IAction.get_Type
: 
---

# IAction::get_Type


## -description


Gets the type of action.

This property is read-only.


## -parameters


## -remarks



The action type is defined when the action is created and cannot be changed later. For information on creating an action, see <a href="https://msdn.microsoft.com/815a000b-ba02-470d-80e6-06ba3c8ea014">IActionCollection.Create</a>.

For information on how actions and tasks work together, see <a href="https://msdn.microsoft.com/4cbe739d-4c4e-4469-8289-4be41b93950c">Task Actions</a>.




## -see-also




<a href="https://msdn.microsoft.com/50d60cf0-642a-43fe-9163-51740e75fa8d">IAction</a>



<a href="https://msdn.microsoft.com/931ea805-fc73-4717-ab40-c12767930df3">TASK_ACTION_TYPE</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

