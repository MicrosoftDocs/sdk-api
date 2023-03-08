---
UID: NN:taskschd.IActionCollection
title: IActionCollection (taskschd.h)
description: Contains the actions that are performed by the task.
helpviewer_keywords: ["IActionCollection","IActionCollection interface [Task Scheduler]","IActionCollection interface [Task Scheduler]","described","actions [Task Scheduler]","collection interface","taskschd.iactioncollection","taskschd/IActionCollection"]
old-location: taskschd\iactioncollection.htm
tech.root: taskschd
ms.assetid: aa7781b6-2600-4af5-95b8-2ac7928946fa
ms.date: 12/05/2018
ms.keywords: IActionCollection, IActionCollection interface [Task Scheduler], IActionCollection interface [Task Scheduler],described, actions [Task Scheduler],collection interface, taskschd.iactioncollection, taskschd/IActionCollection
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
 - IActionCollection
 - taskschd/IActionCollection
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
 - IActionCollection
---

# IActionCollection interface


## -description

Contains the actions that are performed by the task.

## -inheritance

The <b>IActionCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IActionCollection</b> also has these types of members:

## -remarks

When reading or writing XML for a task, the actions of the task are specified in the  <a href="/windows/desktop/TaskSchd/taskschedulerschema-actions-tasktype-element">Actions</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>, <a href="/previous-versions/aa446886(v=vs.85)">Event Trigger Example (C++)</a>, <a href="/windows/desktop/TaskSchd/daily-trigger-example--c---">Daily Trigger Example (C++)</a>, <a href="/windows/desktop/TaskSchd/registration-trigger-example--c---">Registration Trigger Example (C++)</a>, <a href="/windows/desktop/TaskSchd/weekly-trigger-example--c---">Weekly Trigger Example (C++)</a>, <a href="/windows/desktop/TaskSchd/logon-trigger-example--c---">Logon Trigger Example (C++)</a>, or <a href="/windows/desktop/TaskSchd/boot-trigger-example--c---">Boot Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
