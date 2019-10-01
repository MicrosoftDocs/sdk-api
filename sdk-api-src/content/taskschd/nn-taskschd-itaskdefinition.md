---
UID: NN:taskschd.ITaskDefinition
title: ITaskDefinition (taskschd.h)
author: windows-sdk-content
description: Defines all the components of a task, such as the task settings, triggers, actions, and registration information.
old-location: taskschd\itaskdefinition.htm
tech.root: taskschd
ms.assetid: 3787ed9b-9fd0-473b-9034-ade97dc330d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITaskDefinition, ITaskDefinition interface [Task Scheduler], ITaskDefinition interface [Task Scheduler],described, taskschd.itaskdefinition, taskschd/ITaskDefinition
ms.topic: interface
f1_keywords: 
 - "taskschd/ITaskDefinition"
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
 - ITaskDefinition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskDefinition interface


## -description


Defines all the components of a task, such as the task settings, triggers, actions, and registration information.


## -remarks



When reading or writing your own XML for a task, a task definition is specified using the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-task-element">Task</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/previous-versions/aa446886(v=vs.85)">Event Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/daily-trigger-example--c---">Daily Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/registration-trigger-example--c---">Registration Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/weekly-trigger-example--c---">Weekly Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/logon-trigger-example--c---">Logon Trigger Example (C++)</a>, or <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/boot-trigger-example--c---">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_definition">Definition Property of IRegisteredTask</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iactioncollection">IActionCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iprincipal">IPrincipal</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo">IRegistrationInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask">ITaskService::NewTask</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>
 

 

