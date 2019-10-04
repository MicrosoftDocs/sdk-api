---
UID: NN:taskschd.IRegistrationTrigger
title: IRegistrationTrigger (taskschd.h)
author: windows-sdk-content
description: Represents a trigger that starts a task when the task is registered or updated.
old-location: taskschd\iregistrationtrigger.htm
tech.root: taskschd
ms.assetid: 0862f7ac-69d6-4271-8d39-c5bd7038a95e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRegistrationTrigger, IRegistrationTrigger interface [Task Scheduler], IRegistrationTrigger interface [Task Scheduler],described, registration trigger [Task Scheduler],interface, taskschd.iregistrationtrigger, taskschd/IRegistrationTrigger
ms.topic: interface
f1_keywords: 
 - "taskschd/IRegistrationTrigger"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRegistrationTrigger interface


## -description


Represents a trigger that starts a task when the task is registered or updated.


## -remarks



When creating your own XML for a task, a registration trigger is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-registrationtrigger-triggergroup-element">RegistrationTrigger</a> element of the Task Scheduler schema.

If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during  the delay, before the task runs, then the task will not run and the delay will be lost.


#### Examples

For more information and a code example for this interface, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/registration-trigger-example--c---">Registration Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">ITriggerCollection::Create</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

