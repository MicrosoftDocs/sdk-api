---
UID: NN:taskschd.ITaskSettings
title: ITaskSettings (taskschd.h)
description: Provides the settings that the Task Scheduler service uses to perform the task.
old-location: taskschd\itasksettings.htm
tech.root: taskschd
ms.assetid: 203264d1-f67c-45ba-931b-206d7f57a2a6
ms.date: 12/05/2018
ms.keywords: ITaskSettings, ITaskSettings interface [Task Scheduler], ITaskSettings interface [Task Scheduler],described, taskschd.itasksettings, taskschd/ITaskSettings
ms.topic: interface
f1_keywords:
- taskschd/ITaskSettings
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
- ITaskSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskSettings interface


## -description


 Provides the settings that the Task Scheduler service uses to perform the task.


## -remarks



By default, a task will be stopped 72 hours after it starts to run.  You can change this by changing the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit">ExecutionTimeLimit</a> setting.

When reading or writing XML for a task, the task settings are defined in the  <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-settings-tasktype-element">Settings</a> element of the Task Scheduler schema.

When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:

<ul>
<li>Not set to <b>Start the task only if the computer is idle...</b> (task doesn't use <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings">IdleSettings</a>)</li>
<li>Not set to run during automatic maintenance (task doesn't use <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itasksettings3-get_maintenancesettings">MaintenanceSettings</a>)</li>
<li>Is set to <b>Run only when user is logged on</b> (task <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype">LogonType</a> is <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or <b>TASK_LOGON_GROUP</b>)</li>
</ul>
All other triggers are delayed until battery saver is off. For more information about accessing battery saver status in your application, see <a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-system_power_status">SYSTEM_POWER_STATUS</a>. For general information about battery saver, see <a href="https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-saver">battery saver (in the hardware component guidelines)</a>. 


#### Examples

For more information and a code example for this interface, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>.   

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iidlesettings">IIdleSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-inetworksettings">INetworkSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition">ITaskDefinition</a>
 

 

