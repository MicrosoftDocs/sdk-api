---
UID: NE:taskschd._TASK_CREATION
title: "_TASK_CREATION"
author: windows-sdk-content
description: Defines how the Task Scheduler service creates, updates, or disables the task.
old-location: taskschd\taskcreation.htm
old-project: TaskSchd
ms.assetid: e8da4d76-25c8-4209-a75b-c77217c366d4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: TASK_CREATE, TASK_CREATE_OR_UPDATE, TASK_CREATION, TASK_CREATION enumeration [Task Scheduler], TASK_DISABLE, TASK_DONT_ADD_PRINCIPAL_ACE, TASK_IGNORE_REGISTRATION_TRIGGERS, TASK_UPDATE, TASK_VALIDATE_ONLY, _TASK_CREATION, taskschd.taskcreation, taskschd/TASK_CREATE, taskschd/TASK_CREATE_OR_UPDATE, taskschd/TASK_CREATION, taskschd/TASK_DISABLE, taskschd/TASK_DONT_ADD_PRINCIPAL_ACE, taskschd/TASK_IGNORE_REGISTRATION_TRIGGERS, taskschd/TASK_UPDATE, taskschd/TASK_VALIDATE_ONLY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: TASK_CREATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - taskschd.h
api_name:
 - TASK_CREATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _TASK_CREATION enumeration


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

The Task Scheduler service registers the disabled task. A disabled task cannot run until it is enabled. For more information, see <a href="https://msdn.microsoft.com/6c6e7f51-9591-4b84-b06b-124cd88a0345">Enabled Property of ITaskSettings</a> and <a href="https://msdn.microsoft.com/33486621-3984-4a07-8182-c193847a9f76">Enabled Property of IRegisteredTask</a>.


### -field TASK_DONT_ADD_PRINCIPAL_ACE

The Task Scheduler service is prevented from adding the allow access-control entry (ACE) for the context principal. When the <a href="https://msdn.microsoft.com/a94db861-b24e-476a-810d-2cf3bbfc67d1">ITaskFolder::RegisterTaskDefinition</a> or  <a href="https://msdn.microsoft.com/743e5bd9-3fb6-4e09-96ed-ca2d74fa0bab">ITaskFolder::RegisterTask</a> functions are called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.


### -field TASK_IGNORE_REGISTRATION_TRIGGERS

The Task Scheduler service creates the task, but ignores the registration triggers in the task. By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.


## -see-also




<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

