---
UID: NF:taskschd.ITaskSettings.put_IdleSettings
title: ITaskSettings::put_IdleSettings (taskschd.h)
description: Gets or sets the information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition. (Put)
helpviewer_keywords: ["ITaskSettings interface [Task Scheduler]","IdleSettings property","ITaskSettings.IdleSettings","ITaskSettings.put_IdleSettings","ITaskSettings::IdleSettings","ITaskSettings::get_IdleSettings","ITaskSettings::put_IdleSettings","IdleSettings property [Task Scheduler]","IdleSettings property [Task Scheduler]","ITaskSettings interface","put_IdleSettings","taskschd.itasksettings_idlesettings","taskschd/ITaskSettings::IdleSettings","taskschd/ITaskSettings::get_IdleSettings","taskschd/ITaskSettings::put_IdleSettings"]
old-location: taskschd\itasksettings_idlesettings.htm
tech.root: taskschd
ms.assetid: d3bec139-f395-4658-b8be-79b7281c4f93
ms.date: 12/05/2018
ms.keywords: ITaskSettings interface [Task Scheduler],IdleSettings property, ITaskSettings.IdleSettings, ITaskSettings.put_IdleSettings, ITaskSettings::IdleSettings, ITaskSettings::get_IdleSettings, ITaskSettings::put_IdleSettings, IdleSettings property [Task Scheduler], IdleSettings property [Task Scheduler],ITaskSettings interface, put_IdleSettings, taskschd.itasksettings_idlesettings, taskschd/ITaskSettings::IdleSettings, taskschd/ITaskSettings::get_IdleSettings, taskschd/ITaskSettings::put_IdleSettings
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
 - ITaskSettings::put_IdleSettings
 - taskschd/ITaskSettings::put_IdleSettings
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
 - ITaskSettings.IdleSettings
 - ITaskSettings.get_IdleSettings
 - ITaskSettings.put_IdleSettings
---

# ITaskSettings::put_IdleSettings


## -description

Gets or sets the  information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition. For information about idle conditions, see <a href="/windows/desktop/TaskSchd/task-idle-conditions">Task Idle Conditions</a>.

This property is read/write.

## -parameters

## -remarks

When reading or writing  XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-idlesettings-settingstype-element">IdleSettings</a> element of the Task Scheduler schema.

When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:

<ul>
<li>Not set to <b>Start the task only if the computer is idle...</b> (task doesn't use <b>IdleSettings</b>)</li>
<li>Not set to run during automatic maintenance (task doesn't use <a href="/windows/desktop/api/taskschd/nf-taskschd-itasksettings3-get_maintenancesettings">MaintenanceSettings</a>)</li>
<li>Is set to <b>Run only when user is logged on</b> (task <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype">LogonType</a> is <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or <b>TASK_LOGON_GROUP</b>)</li>
</ul>
All other triggers are delayed until battery saver is off. For more information about accessing battery saver status in your application, see <a href="/windows/desktop/api/winbase/ns-winbase-system_power_status">SYSTEM_POWER_STATUS</a>. For general information about battery saver, see <a href="/windows-hardware/design/component-guidelines/battery-saver">battery saver (in the hardware component guidelines)</a>.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
