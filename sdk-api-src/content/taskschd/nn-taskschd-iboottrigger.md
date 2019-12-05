---
UID: NN:taskschd.IBootTrigger
title: IBootTrigger (taskschd.h)
description: Represents a trigger that starts a task when the system is started.
old-location: taskschd\iboottrigger.htm
tech.root: taskschd
ms.assetid: 8f186ee2-8d74-426c-9173-523a335422c9
ms.date: 12/05/2018
ms.keywords: IBootTrigger, IBootTrigger interface [Task Scheduler], IBootTrigger interface [Task Scheduler],described, boot trigger [Task Scheduler],interface, taskschd.iboottrigger, taskschd/IBootTrigger
ms.topic: interface
f1_keywords:
- taskschd/IBootTrigger
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
- IBootTrigger
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBootTrigger interface


## -description


Represents a trigger that starts a task when the system is started.


## -remarks



The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.

Only a member of the Administrators group can create a task with a boot trigger.

When creating your own XML for a task, a boot trigger is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-boottrigger-triggergroup-element">BootTrigger</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/boot-trigger-example--c---">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

