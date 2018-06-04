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
 

 

