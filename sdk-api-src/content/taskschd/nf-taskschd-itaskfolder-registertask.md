---
UID: NF:taskschd.ITaskFolder.RegisterTask
title: ITaskFolder::RegisterTask (taskschd.h)
description: Registers (creates) a new task in the folder using XML to define the task.
helpviewer_keywords: ["ITaskFolder interface [Task Scheduler]","RegisterTask method","ITaskFolder.RegisterTask","ITaskFolder::RegisterTask","RegisterTask","RegisterTask method [Task Scheduler]","RegisterTask method [Task Scheduler]","ITaskFolder interface","TASK_CREATE","TASK_CREATE_OR_UPDATE","TASK_DISABLE","TASK_DONT_ADD_PRINCIPAL_ACE","TASK_IGNORE_REGISTRATION_TRIGGERS","TASK_LOGON_GROUP","TASK_LOGON_INTERACTIVE_TOKEN","TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD","TASK_LOGON_NONE","TASK_LOGON_PASSWORD","TASK_LOGON_S4U","TASK_LOGON_SERVICE_ACCOUNT","TASK_UPDATE","TASK_VALIDATE_ONLY","taskschd.itaskfolder_registertask","taskschd/ITaskFolder::RegisterTask"]
old-location: taskschd\itaskfolder_registertask.htm
tech.root: taskschd
ms.assetid: 743e5bd9-3fb6-4e09-96ed-ca2d74fa0bab
ms.date: 12/05/2018
ms.keywords: ITaskFolder interface [Task Scheduler],RegisterTask method, ITaskFolder.RegisterTask, ITaskFolder::RegisterTask, RegisterTask, RegisterTask method [Task Scheduler], RegisterTask method [Task Scheduler],ITaskFolder interface, TASK_CREATE, TASK_CREATE_OR_UPDATE, TASK_DISABLE, TASK_DONT_ADD_PRINCIPAL_ACE, TASK_IGNORE_REGISTRATION_TRIGGERS, TASK_LOGON_GROUP, TASK_LOGON_INTERACTIVE_TOKEN, TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD, TASK_LOGON_NONE, TASK_LOGON_PASSWORD, TASK_LOGON_S4U, TASK_LOGON_SERVICE_ACCOUNT, TASK_UPDATE, TASK_VALIDATE_ONLY, taskschd.itaskfolder_registertask, taskschd/ITaskFolder::RegisterTask
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
 - ITaskFolder::RegisterTask
 - taskschd/ITaskFolder::RegisterTask
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
 - ITaskFolder.RegisterTask
---

# ITaskFolder::RegisterTask


## -description

Registers (creates) a new task in the folder using XML to define the task.

## -parameters

### -param path [in]

The task name. If this value is <b>NULL</b>, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.

A task name cannot begin or end with a space character. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.

### -param xmlText [in]

An XML-formatted definition of the task.

The following topics contain tasks defined using XML.<ul>
<li>
<a href="/windows/desktop/TaskSchd/time-trigger-example--xml-">Time Trigger Example (XML)</a>
</li>
<li>
<a href="/previous-versions/aa446889(v=vs.85)">Event Trigger Example (XML)</a>
</li>
<li>
<a href="/windows/desktop/TaskSchd/daily-trigger-example--xml-">Daily Trigger Example (XML)</a>
</li>
<li>
<a href="/windows/desktop/TaskSchd/registration-trigger-example--xml-">Registration Trigger Example (XML)</a>
</li>
<li>
<a href="/windows/desktop/TaskSchd/weekly-trigger-example--xml-">Weekly Trigger Example (XML)</a>
</li>
<li>
<a href="/windows/desktop/TaskSchd/logon-trigger-example--xml-">Logon Trigger Example (XML)</a>
</li>
<li>
<a href="/windows/desktop/TaskSchd/boot-trigger-example--xml-">Boot Trigger Example (XML)</a>
</li>
</ul>

### -param flags [in]

A <a href="/windows/desktop/api/taskschd/ne-taskschd-task_creation">TASK_CREATION</a> constant.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TASK_VALIDATE_ONLY"></a><a id="task_validate_only"></a><dl>
<dt><b>TASK_VALIDATE_ONLY</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The Task Scheduler verifies the syntax of the XML that describes the task, but does not register the task. This constant cannot be combined with the <b>TASK_CREATE</b>, <b>TASK_UPDATE</b>, or  <b>TASK_CREATE_OR_UPDATE</b> values.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_CREATE"></a><a id="task_create"></a><dl>
<dt><b>TASK_CREATE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Task Scheduler registers the task as a new task.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_UPDATE"></a><a id="task_update"></a><dl>
<dt><b>TASK_UPDATE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Task Scheduler registers the task as an updated version of an existing task. When a task with a registration trigger is updated, the task will execute after the update occurs.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_CREATE_OR_UPDATE"></a><a id="task_create_or_update"></a><dl>
<dt><b>TASK_CREATE_OR_UPDATE</b></dt>
<dt>0x6</dt>
</dl>
</td>
<td width="60%">
Task Scheduler either registers the task as a new task or as an updated version if the task already exists. Equivalent to TASK_CREATE | TASK_UPDATE.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_DISABLE"></a><a id="task_disable"></a><dl>
<dt><b>TASK_DISABLE</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Task Scheduler disables the existing task.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_DONT_ADD_PRINCIPAL_ACE"></a><a id="task_dont_add_principal_ace"></a><dl>
<dt><b>TASK_DONT_ADD_PRINCIPAL_ACE</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal. When the <b>ITaskFolder::RegisterTask</b> function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_IGNORE_REGISTRATION_TRIGGERS"></a><a id="task_ignore_registration_triggers"></a><dl>
<dt><b>TASK_IGNORE_REGISTRATION_TRIGGERS</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
The Task Scheduler creates the task, but ignores the registration triggers in the task. By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.

</td>
</tr>
</table>

### -param userId [in]

The user credentials used to register the task.

<div class="alert"><b>Note</b>  If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter. A task is defined as a Task Scheduler 1.0 task when the version attribute of the Task element in the task's XML is set to 1.1.</div>
<div> </div>

### -param password [in]

The password for the userId used to register the task. When the TASK_LOGON_SERVICE_ACCOUNT logon type is used, the password must be an empty <b>VARIANT</b> value such as <b>VT_NULL</b> or <b>VT_EMPTY</b>.

### -param logonType [in]

A value that defines what logon technique is used to run the registered task.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TASK_LOGON_NONE"></a><a id="task_logon_none"></a><dl>
<dt><b>TASK_LOGON_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The logon method is not specified. Used for non-NT credentials.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_LOGON_PASSWORD"></a><a id="task_logon_password"></a><dl>
<dt><b>TASK_LOGON_PASSWORD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use a password for logging on the user. The password must be supplied at registration time.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_LOGON_S4U"></a><a id="task_logon_s4u"></a><dl>
<dt><b>TASK_LOGON_S4U</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Use an existing interactive token to run a task. The user must log on using a service for user (S4U) logon. When an S4U logon is used, no password is stored by the system and there is no access to either the network or  to encrypted files.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_LOGON_INTERACTIVE_TOKEN"></a><a id="task_logon_interactive_token"></a><dl>
<dt><b>TASK_LOGON_INTERACTIVE_TOKEN</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
 User must already be logged on. The task will be run only in an existing interactive session.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_LOGON_GROUP"></a><a id="task_logon_group"></a><dl>
<dt><b>TASK_LOGON_GROUP</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Group activation. The <b>groupId</b> field specifies the group.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_LOGON_SERVICE_ACCOUNT"></a><a id="task_logon_service_account"></a><dl>
<dt><b>TASK_LOGON_SERVICE_ACCOUNT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Indicates that a Local System, Local Service, or Network Service account is used as a security context to run the task.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></a><a id="task_logon_interactive_token_or_password"></a><dl>
<dt><b>TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
First use the interactive token.  If the user is not logged on (no interactive token is available), then the password is used.  The password must be specified when a task is registered. This flag is not recommended for new tasks because it is less reliable than <b>TASK_LOGON_PASSWORD</b>.

</td>
</tr>
</table>

### -param sddl [in, optional]

The security descriptor associated with the registered task. You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.

<div class="alert"><b>Note</b>   If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</div>
<div> </div>

### -param ppTask [out]

An <a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a> interface that represents the new task.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESS_DENIED</b></dt>
<dt>0x80070005</dt>
</dl>
</td>
<td width="60%">
Access is denied to connect to the Task Scheduler service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>0x8007000e</dt>
</dl>
</td>
<td width="60%">
The application does not have enough memory to complete the operation or the <i>user</i> or <i>password</i> has at least one null and one non-null value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_S_BATCH_LOGON_PROBLEM</b></dt>
<dt>0x0004131C</dt>
</dl>
</td>
<td width="60%">
The task is registered, but may fail to start. Batch logon privilege needs to be enabled for the task principal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_S_SOME_TRIGGERS_FAILED</b></dt>
<dt>0x0004131B</dt>
</dl>
</td>
<td width="60%">
The task is registered, but not all specified triggers will start the task.

</td>
</tr>
</table>

## -remarks

For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.  To set the task logon type to be interactive, specify <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or  <b>TASK_LOGON_GROUP</b> in the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype">LogonType</a> property of the task principal, or in the <i>logonType</i> parameter of <b>ITaskFolder::RegisterTask</b> or <a href="/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition">ITaskFolder::RegisterTaskDefinition</a>. 

Only a member of the Administrators group can create a task with a boot trigger.

You can successfully register a task with a group specified in the <i>userId</i> parameter and <b>TASK_LOGON_INTERACTIVE_TOKEN</b> specified in the <i>logonType</i> parameter of <b>ITaskFolder::RegisterTask</b> or <a href="/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition">ITaskFolder::RegisterTaskDefinition</a>, but the task will not run.

Passing the TASK_VALIDATE_ONLY and TASK_IGNORE_REGISTRATION_TRIGGERS values together to the <i>flags</i> parameter is an invalid argument.

If a task defines a network that does not exist in the <a href="/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings">NetworkSettings</a> settings of the task, the <b>ITaskFolder::RegisterTask</b>  method will return error 0x8000ffff when the task is registered.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>