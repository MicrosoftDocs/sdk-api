---
UID: NN:taskschd.IRegistrationTrigger
title: IRegistrationTrigger
author: windows-sdk-content
description: Represents a trigger that starts a task when the task is registered or updated.
old-location: taskschd\iregistrationtrigger.htm
tech.root: taskschd
ms.assetid: 0862f7ac-69d6-4271-8d39-c5bd7038a95e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRegistrationTrigger, IRegistrationTrigger interface [Task Scheduler], IRegistrationTrigger interface [Task Scheduler],described, registration trigger [Task Scheduler],interface, taskschd.iregistrationtrigger, taskschd/IRegistrationTrigger
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRegistrationTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRegistrationTrigger interface


## -description


Represents a trigger that starts a task when the task is registered or updated.


## -remarks



When creating your own XML for a task, a registration trigger is specified using the <a href="https://msdn.microsoft.com/8f028ed0-93e6-4423-be2f-9a02be99122b">RegistrationTrigger</a> element of the Task Scheduler schema.

If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during  the delay, before the task runs, then the task will not run and the delay will be lost.


#### Examples

For more information and a code example for this interface, see <a href="https://msdn.microsoft.com/5e2e8fa6-66c7-4356-8fd6-22f7974791b9">Registration Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>



<a href="https://msdn.microsoft.com/70780fca-ba97-42b8-bc00-867c2761953c">ITriggerCollection::Create</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

