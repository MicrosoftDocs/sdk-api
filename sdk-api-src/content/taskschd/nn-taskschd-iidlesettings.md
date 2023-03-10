---
UID: NN:taskschd.IIdleSettings
title: IIdleSettings (taskschd.h)
description: Specifies how the Task Scheduler performs tasks when the computer is in an idle condition.
helpviewer_keywords: ["IIdleSettings","IIdleSettings interface [Task Scheduler]","IIdleSettings interface [Task Scheduler]","described","taskschd.iidlesettings","taskschd/IIdleSettings"]
old-location: taskschd\iidlesettings.htm
tech.root: taskschd
ms.assetid: a6bd9278-b9ac-4eb3-957a-5191cee12a6f
ms.date: 12/05/2018
ms.keywords: IIdleSettings, IIdleSettings interface [Task Scheduler], IIdleSettings interface [Task Scheduler],described, taskschd.iidlesettings, taskschd/IIdleSettings
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
 - IIdleSettings
 - taskschd/IIdleSettings
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
 - IIdleSettings
---

# IIdleSettings interface


## -description

Specifies how the Task Scheduler performs tasks when the computer is in an idle condition. For information about idle conditions, see <a href="/windows/desktop/TaskSchd/task-idle-conditions">Task Idle Conditions</a>.

## -remarks

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-idlesettings-settingstype-element">IdleSettings</a> element of the Task Scheduler schema.

If a task is triggered by an idle trigger, then the <a href="/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout">WaitTimeout</a> property of the <b>IIdleSettings</b> interface is ignored.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>