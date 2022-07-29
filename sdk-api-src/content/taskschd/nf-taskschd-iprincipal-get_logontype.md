---
UID: NF:taskschd.IPrincipal.get_LogonType
title: IPrincipal::get_LogonType (taskschd.h)
description: Gets or sets the security logon method that is required to run the tasks that are associated with the principal. (Get)
helpviewer_keywords: ["IPrincipal interface [Task Scheduler]","LogonType property","IPrincipal.LogonType","IPrincipal.get_LogonType","IPrincipal::LogonType","IPrincipal::get_LogonType","IPrincipal::put_LogonType","LogonType property [Task Scheduler]","LogonType property [Task Scheduler]","IPrincipal interface","TASK_LOGON_GROUP","TASK_LOGON_INTERACTIVE_TOKEN","TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD","TASK_LOGON_NONE","TASK_LOGON_PASSWORD","TASK_LOGON_S4U","TASK_LOGON_SERVICE_ACCOUNT","get_LogonType","taskschd.iprincipal_logontype","taskschd/IPrincipal::LogonType","taskschd/IPrincipal::get_LogonType","taskschd/IPrincipal::put_LogonType"]
old-location: taskschd\iprincipal_logontype.htm
tech.root: taskschd
ms.assetid: cf0a8ad4-f1bb-46a2-ae92-d00e08b8d459
ms.date: 12/05/2018
ms.keywords: IPrincipal interface [Task Scheduler],LogonType property, IPrincipal.LogonType, IPrincipal.get_LogonType, IPrincipal::LogonType, IPrincipal::get_LogonType, IPrincipal::put_LogonType, LogonType property [Task Scheduler], LogonType property [Task Scheduler],IPrincipal interface, TASK_LOGON_GROUP, TASK_LOGON_INTERACTIVE_TOKEN, TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD, TASK_LOGON_NONE, TASK_LOGON_PASSWORD, TASK_LOGON_S4U, TASK_LOGON_SERVICE_ACCOUNT, get_LogonType, taskschd.iprincipal_logontype, taskschd/IPrincipal::LogonType, taskschd/IPrincipal::get_LogonType, taskschd/IPrincipal::put_LogonType
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
 - IPrincipal::get_LogonType
 - taskschd/IPrincipal::get_LogonType
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
 - IPrincipal.LogonType
 - IPrincipal.get_LogonType
 - IPrincipal.put_LogonType
---

# IPrincipal::get_LogonType


## -description

Gets or sets the security logon method that is required  to run the tasks that are associated with the principal.

This property is read/write.

## -parameters

## -remarks

This property is valid only when a user identifier is specified by the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid">UserId</a> property.

When reading or writing XML for a task, the logon type is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-logontype-principaltype-element">&lt;LogonType&gt;</a> element of the Task Scheduler schema.

For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.  To set the task logon type to be interactive, specify <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or  <b>TASK_LOGON_GROUP</b> in the <b>LogonType</b> property of the task principal, or in the <i>logonType</i> parameter of <a href="/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask">ITaskFolder::RegisterTask</a> or <a href="/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition">ITaskFolder::RegisterTaskDefinition</a>. 

When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:

<ul>
<li>Not set to <b>Start the task only if the computer is idle...</b> (task doesn't use <a href="/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings">IdleSettings</a>)</li>
<li>Not set to run during automatic maintenance (task doesn't use <a href="/windows/desktop/api/taskschd/nf-taskschd-itasksettings3-get_maintenancesettings">MaintenanceSettings</a>)</li>
<li>Is set to <b>Run only when user is logged on</b> (task <b>LogonType</b> is <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or <b>TASK_LOGON_GROUP</b>)</li>
</ul>
All other triggers are delayed until battery saver is off. For more information about accessing battery saver status in your application, see <a href="/windows/desktop/api/winbase/ns-winbase-system_power_status">SYSTEM_POWER_STATUS</a>. For general information about battery saver, see <a href="/windows-hardware/design/component-guidelines/battery-saver">battery saver (in the hardware component guidelines)</a>.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iprincipal">IPrincipal</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
