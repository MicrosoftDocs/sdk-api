---
UID: NF:taskschd.IAction.get_Type
title: IAction::get_Type (taskschd.h)
description: Gets the type of action.
helpviewer_keywords: ["IAction interface [Task Scheduler]","Type property","IAction.Type","IAction.get_Type","IAction::Type","IAction::get_Type","TASK_ACTION_COM_HANDLER","TASK_ACTION_EXEC","TASK_ACTION_SEND_EMAIL","TASK_ACTION_SHOW_MESSAGE","Type property [Task Scheduler]","Type property [Task Scheduler]","IAction interface","get_Type","taskschd.iaction_type","taskschd/IAction::Type","taskschd/IAction::get_Type"]
old-location: taskschd\iaction_type.htm
tech.root: taskschd
ms.assetid: 720aae58-b58c-4948-9e94-94c5a041a2db
ms.date: 12/05/2018
ms.keywords: IAction interface [Task Scheduler],Type property, IAction.Type, IAction.get_Type, IAction::Type, IAction::get_Type, TASK_ACTION_COM_HANDLER, TASK_ACTION_EXEC, TASK_ACTION_SEND_EMAIL, TASK_ACTION_SHOW_MESSAGE, Type property [Task Scheduler], Type property [Task Scheduler],IAction interface, get_Type, taskschd.iaction_type, taskschd/IAction::Type, taskschd/IAction::get_Type
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAction::get_Type
 - taskschd/IAction::get_Type
dev_langs:
 - c++
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
---

# IAction::get_Type


## -description

Gets the type of action.

This property is read-only.

## -parameters

## -remarks

The action type is defined when the action is created and cannot be changed later. For information on creating an action, see <a href="/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create">IActionCollection.Create</a>.

For information on how actions and tasks work together, see <a href="/windows/desktop/TaskSchd/task-actions">Task Actions</a>.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a>



<a href="/windows/desktop/api/taskschd/ne-taskschd-task_action_type">TASK_ACTION_TYPE</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>