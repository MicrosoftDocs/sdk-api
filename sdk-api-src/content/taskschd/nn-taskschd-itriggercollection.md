---
UID: NN:taskschd.ITriggerCollection
title: ITriggerCollection (taskschd.h)
description: Provides the methods that are used to add to, remove from, and get the triggers of a task.
helpviewer_keywords: ["ITriggerCollection","ITriggerCollection interface [Task Scheduler]","ITriggerCollection interface [Task Scheduler]","described","taskschd.itriggercollection","taskschd/ITriggerCollection","triggers [Task Scheduler]","trigger collection interface"]
old-location: taskschd\itriggercollection.htm
tech.root: taskschd
ms.assetid: 5985ff67-3aa2-4ade-9d53-da4d640f5f6e
ms.date: 12/05/2018
ms.keywords: ITriggerCollection, ITriggerCollection interface [Task Scheduler], ITriggerCollection interface [Task Scheduler],described, taskschd.itriggercollection, taskschd/ITriggerCollection, triggers [Task Scheduler],trigger collection interface
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
 - ITriggerCollection
 - taskschd/ITriggerCollection
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
 - ITriggerCollection
---

# ITriggerCollection interface


## -description

Provides the methods that are used to add to, remove from, and get the triggers of a task.

## -inheritance

The <b>ITriggerCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITriggerCollection</b> also has these types of members:

## -remarks

When reading or writing XML for a task, the triggers for the task are specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-triggers-tasktype-element">Triggers</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>, <a href="/previous-versions/aa446886(v=vs.85)">Event Trigger Example (C++)</a>, <a href="/windows/desktop/TaskSchd/daily-trigger-example--c---">Daily Trigger Example (C++)</a>, <a href="/windows/desktop/TaskSchd/registration-trigger-example--c---">Registration Trigger Example (C++)</a>, <a href="/windows/desktop/TaskSchd/weekly-trigger-example--c---">Weekly Trigger Example (C++)</a>, <a href="/windows/desktop/TaskSchd/logon-trigger-example--c---">Logon Trigger Example (C++)</a>, or <a href="/windows/desktop/TaskSchd/boot-trigger-example--c---">Boot Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
