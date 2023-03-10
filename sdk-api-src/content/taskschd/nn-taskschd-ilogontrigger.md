---
UID: NN:taskschd.ILogonTrigger
title: ILogonTrigger (taskschd.h)
description: Represents a trigger that starts a task when a user logs on.
helpviewer_keywords: ["ILogonTrigger","ILogonTrigger interface [Task Scheduler]","ILogonTrigger interface [Task Scheduler]","described","logon trigger [Task Scheduler]","interface","taskschd.ilogontrigger","taskschd/ILogonTrigger"]
old-location: taskschd\ilogontrigger.htm
tech.root: taskschd
ms.assetid: c0206a18-53f2-4def-8f54-2b175a0579f4
ms.date: 12/05/2018
ms.keywords: ILogonTrigger, ILogonTrigger interface [Task Scheduler], ILogonTrigger interface [Task Scheduler],described, logon trigger [Task Scheduler],interface, taskschd.ilogontrigger, taskschd/ILogonTrigger
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
 - ILogonTrigger
 - taskschd/ILogonTrigger
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
 - ILogonTrigger
---

# ILogonTrigger interface


## -description

Represents a trigger that starts a task when a user logs on. When the Task Scheduler service starts, all logged-on users are enumerated and any tasks registered with logon triggers that match the logged on user are run.

## -remarks

If you want a task to be triggered when any member of a group logs on to the computer rather than when  a specific user logs on, then do not assign a value to the  <a href="/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid">UserId</a> property.  Instead, create a logon trigger with an empty <b>UserId</b> property and assign a value to the principal for the task using the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid">GroupId</a> property.

When reading or writing XML for a task, a logon trigger is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-logontrigger-triggergroup-element">LogonTrigger</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/logon-trigger-example--c---">Logon Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>