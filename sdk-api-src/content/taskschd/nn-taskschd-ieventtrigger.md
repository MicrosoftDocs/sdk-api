---
UID: NN:taskschd.IEventTrigger
title: IEventTrigger (taskschd.h)
author: windows-sdk-content
description: Represents a trigger that starts a task when a system event occurs.
old-location: taskschd\ieventtrigger.htm
tech.root: taskschd
ms.assetid: 23b7ecb9-d2bb-441a-8c93-126c833f99b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEventTrigger, IEventTrigger interface [Task Scheduler], IEventTrigger interface [Task Scheduler],described, event trigger [Task Scheduler],interface, taskschd.ieventtrigger, taskschd/IEventTrigger
ms.topic: interface
f1_keywords:
- taskschd/IEventTrigger
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
- IEventTrigger
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventTrigger interface


## -description


Represents a trigger that starts a task when a system event occurs.


## -remarks



A maximum of 500 tasks with event subscriptions can be created. An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.

When reading or writing your own XML for a task, an event trigger is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-eventtrigger-triggergroup-element">EventTrigger</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://docs.microsoft.com/previous-versions/aa446886(v=vs.85)">Event Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern">IRepetitionPattern</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction">IShowMessageAction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluecollection">ITaskNamedValueCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2">TASK_TRIGGER_TYPE2</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

