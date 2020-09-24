---
UID: NN:taskschd.IIdleTrigger
title: IIdleTrigger (taskschd.h)
description: Represents a trigger that starts a task when the computer goes into an idle state.
helpviewer_keywords: ["IIdleTrigger","IIdleTrigger interface [Task Scheduler]","IIdleTrigger interface [Task Scheduler]","described","idle trigger [Task Scheduler]","interface","taskschd.iidletrigger","taskschd/IIdleTrigger"]
old-location: taskschd\iidletrigger.htm
tech.root: taskschd
ms.assetid: aca5305f-68fc-4211-9f71-3f572340e94d
ms.date: 12/05/2018
ms.keywords: IIdleTrigger, IIdleTrigger interface [Task Scheduler], IIdleTrigger interface [Task Scheduler],described, idle trigger [Task Scheduler],interface, taskschd.iidletrigger, taskschd/IIdleTrigger
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
 - IIdleTrigger
 - taskschd/IIdleTrigger
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
 - IIdleTrigger
---

# IIdleTrigger interface


## -description

Represents a trigger that starts a task when the computer goes into an idle state. For information about idle conditions, see <a href="/windows/desktop/TaskSchd/task-idle-conditions">Task Idle Conditions</a>.

## -remarks

An idle trigger will only trigger a task action if the computer goes into an idle state after the start boundary of the trigger.


When creating your own XML for a task, an idle trigger is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-idletrigger-triggergroup-element">IdleTrigger</a> element of the Task Scheduler schema.

If a task is triggered by an idle trigger, then the <a href="/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout">WaitTimeout</a> property of the <a href="/windows/desktop/api/taskschd/nn-taskschd-iidlesettings">IIdleSettings</a> interface is ignored.

If the initial instance of a task with an idle trigger is still running, then the task is only launched once with no repetitions, even if multiple repetition is defined in the <a href="/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition">Repetition</a> property. This behavior does not occur if the task stops by itself.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>