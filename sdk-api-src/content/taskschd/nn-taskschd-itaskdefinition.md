---
UID: NN:taskschd.ITaskDefinition
title: ITaskDefinition (taskschd.h)
author: windows-sdk-content
description: Defines all the components of a task, such as the task settings, triggers, actions, and registration information.
old-location: taskschd\itaskdefinition.htm
tech.root: taskschd
ms.assetid: 3787ed9b-9fd0-473b-9034-ade97dc330d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITaskDefinition, ITaskDefinition interface [Task Scheduler], ITaskDefinition interface [Task Scheduler],described, taskschd.itaskdefinition, taskschd/ITaskDefinition
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
 - ITaskDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskDefinition interface


## -description


Defines all the components of a task, such as the task settings, triggers, actions, and registration information.


## -remarks



When reading or writing your own XML for a task, a task definition is specified using the <a href="https://msdn.microsoft.com/103a332a-8620-4e0c-81b5-4782d85fc391">Task</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/cacc1b72-7c58-4117-b204-ddb3a312bb08">Event Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/f1038142-b83e-4159-9a7b-db2ae4ed3bd2">Daily Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/5e2e8fa6-66c7-4356-8fd6-22f7974791b9">Registration Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/7c70b743-aff2-4ef5-b65b-ef0b5fdacade">Weekly Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/15647234-8d1f-4d75-b215-92927b300c1f">Logon Trigger Example (C++)</a>, or <a href="https://msdn.microsoft.com/d4dbbfe5-bde9-4a1c-8e11-24cd1e14646c">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/673d5e11-d2a3-4dcb-ad2e-46940574ba92">Definition Property of IRegisteredTask</a>



<a href="https://msdn.microsoft.com/aa7781b6-2600-4af5-95b8-2ac7928946fa">IActionCollection</a>



<a href="https://msdn.microsoft.com/7aa22af2-7f0a-41c1-89c6-d813780e89bf">IPrincipal</a>



<a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a>



<a href="https://msdn.microsoft.com/e04f0c47-ab89-49e4-aac6-028d2555ecf1">IRegistrationInfo</a>



<a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a>



<a href="https://msdn.microsoft.com/821fc610-cf94-4548-950d-b4fd7b2f90dc">ITaskService::NewTask</a>



<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>
 

 

