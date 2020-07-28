---
UID: NE:taskschd._TASK_CREATION
title: TASK_CREATION (taskschd.h)
description: Defines how the Task Scheduler service creates, updates, or disables the task.
helpviewer_keywords: ["TASK_CREATE","TASK_CREATE_OR_UPDATE","TASK_CREATION","TASK_CREATION enumeration [Task Scheduler]","TASK_DISABLE","TASK_DONT_ADD_PRINCIPAL_ACE","TASK_IGNORE_REGISTRATION_TRIGGERS","TASK_UPDATE","TASK_VALIDATE_ONLY","taskschd.taskcreation","taskschd/TASK_CREATE","taskschd/TASK_CREATE_OR_UPDATE","taskschd/TASK_CREATION","taskschd/TASK_DISABLE","taskschd/TASK_DONT_ADD_PRINCIPAL_ACE","taskschd/TASK_IGNORE_REGISTRATION_TRIGGERS","taskschd/TASK_UPDATE","taskschd/TASK_VALIDATE_ONLY"]
old-location: taskschd\taskcreation.htm
tech.root: taskschd
ms.assetid: e8da4d76-25c8-4209-a75b-c77217c366d4
ms.date: 12/05/2018
ms.keywords: TASK_CREATE, TASK_CREATE_OR_UPDATE, TASK_CREATION, TASK_CREATION enumeration [Task Scheduler], TASK_DISABLE, TASK_DONT_ADD_PRINCIPAL_ACE, TASK_IGNORE_REGISTRATION_TRIGGERS, TASK_UPDATE, TASK_VALIDATE_ONLY, taskschd.taskcreation, taskschd/TASK_CREATE, taskschd/TASK_CREATE_OR_UPDATE, taskschd/TASK_CREATION, taskschd/TASK_DISABLE, taskschd/TASK_DONT_ADD_PRINCIPAL_ACE, taskschd/TASK_IGNORE_REGISTRATION_TRIGGERS, taskschd/TASK_UPDATE, taskschd/TASK_VALIDATE_ONLY
f1_keywords:
- taskschd/TASK_CREATION
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
- TASK_CREATION
targetos: Windows
req.typenames: TASK_CREATION
req.redist: 
ms.custom: 19H1
---

# TASK_CREATION enumeration


## -description


Defines how the Task Scheduler service creates, updates, or disables the task.


## -enum-fields




### -field TASK_VALIDATE_ONLY

The Task Scheduler service checks the syntax of the XML that describes the task but does not register the task. This constant cannot be combined with the <b>TASK_CREATE</b>, <b>TASK_UPDATE</b>, or  <b>TASK_CREATE_OR_UPDATE</b> values.


### -field TASK_CREATE

The Task Scheduler service registers the task as a new task.


### -field TASK_UPDATE

The Task Scheduler service registers the task as an updated version of an existing task. When a task with a registration trigger is updated, the task will execute after the update occurs.


### -field TASK_CREATE_OR_UPDATE

The Task Scheduler service either registers the task as a new task or as an updated version if the task already exists. Equivalent to TASK_CREATE | TASK_UPDATE.


### -field TASK_DISABLE

The Task Scheduler service registers the disabled task. A disabled task cannot run until it is enabled. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled">Enabled Property of ITaskSettings</a> and <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_enabled">Enabled Property of IRegisteredTask</a>.


### -field TASK_DONT_ADD_PRINCIPAL_ACE

The Task Scheduler service is prevented from adding the allow access-control entry (ACE) for the context principal. When the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition">ITaskFolder::RegisterTaskDefinition</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask">ITaskFolder::RegisterTask</a> functions are called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.


### -field TASK_IGNORE_REGISTRATION_TRIGGERS

The Task Scheduler service creates the task, but ignores the registration triggers in the task. By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
 

 

