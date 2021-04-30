---
UID: NN:taskschd.IBootTrigger
title: IBootTrigger (taskschd.h)
description: Represents a trigger that starts a task when the system is started.
helpviewer_keywords: ["IBootTrigger","IBootTrigger interface [Task Scheduler]","IBootTrigger interface [Task Scheduler]","described","boot trigger [Task Scheduler]","interface","taskschd.iboottrigger","taskschd/IBootTrigger"]
old-location: taskschd\iboottrigger.htm
tech.root: taskschd
ms.assetid: 8f186ee2-8d74-426c-9173-523a335422c9
ms.date: 12/05/2018
ms.keywords: IBootTrigger, IBootTrigger interface [Task Scheduler], IBootTrigger interface [Task Scheduler],described, boot trigger [Task Scheduler],interface, taskschd.iboottrigger, taskschd/IBootTrigger
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
 - IBootTrigger
 - taskschd/IBootTrigger
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
 - IBootTrigger
---

# IBootTrigger interface


## -description

Represents a trigger that starts a task when the system is started.

## -remarks

The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.

Only a member of the Administrators group can create a task with a boot trigger.

When creating your own XML for a task, a boot trigger is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-boottrigger-triggergroup-element">BootTrigger</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/boot-trigger-example--c---">Boot Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>