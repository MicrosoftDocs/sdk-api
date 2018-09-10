---
UID: NF:taskschd.IPrincipal.get_LogonType
title: IPrincipal::get_LogonType
author: windows-sdk-content
description: Gets or sets the security logon method that is required to run the tasks that are associated with the principal.
old-location: taskschd\iprincipal_logontype.htm
tech.root: TaskSchd
ms.assetid: cf0a8ad4-f1bb-46a2-ae92-d00e08b8d459
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPrincipal interface [Task Scheduler],LogonType property, IPrincipal.LogonType, IPrincipal.get_LogonType, IPrincipal::LogonType, IPrincipal::get_LogonType, IPrincipal::put_LogonType, LogonType property [Task Scheduler], LogonType property [Task Scheduler],IPrincipal interface, TASK_LOGON_GROUP, TASK_LOGON_INTERACTIVE_TOKEN, TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD, TASK_LOGON_NONE, TASK_LOGON_PASSWORD, TASK_LOGON_S4U, TASK_LOGON_SERVICE_ACCOUNT, get_LogonType, taskschd.iprincipal_logontype, taskschd/IPrincipal::LogonType, taskschd/IPrincipal::get_LogonType, taskschd/IPrincipal::put_LogonType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IPrincipal.LogonType
 - IPrincipal.get_LogonType
 - IPrincipal.put_LogonType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrincipal::get_LogonType


## -description


Gets or sets the security logon method that is required  to run the tasks that are associated with the principal.

This property is read/write.


## -parameters


## -remarks



This property is valid only when a user identifier is specified by the <a href="https://msdn.microsoft.com/b85a1f05-acb0-4b3c-bea0-393ad7c6a43d">UserId</a> property.

When reading or writing XML for a task, the logon type is specified in the <a href="https://msdn.microsoft.com/e36a1755-96f3-45dc-8779-8bd0cfde886c"><LogonType></a> element of the Task Scheduler schema.

For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.  To set the task logon type to be interactive, specify <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or  <b>TASK_LOGON_GROUP</b> in the <b>LogonType</b> property of the task principal, or in the <i>logonType</i> parameter of <a href="https://msdn.microsoft.com/743e5bd9-3fb6-4e09-96ed-ca2d74fa0bab">ITaskFolder::RegisterTask</a> or <a href="https://msdn.microsoft.com/a94db861-b24e-476a-810d-2cf3bbfc67d1">ITaskFolder::RegisterTaskDefinition</a>. 

When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:

<ul>
<li>Not set to <b>Start the task only if the computer is idle...</b> (task doesn't use <a href="https://msdn.microsoft.com/d3bec139-f395-4658-b8be-79b7281c4f93">IdleSettings</a>)</li>
<li>Not set to run during automatic maintenance (task doesn't use <a href="https://msdn.microsoft.com/F4B6ED81-DE9A-42C8-8F16-D5BD93743CB3">MaintenanceSettings</a>)</li>
<li>Is set to <b>Run only when user is logged on</b> (task <b>LogonType</b> is <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or <b>TASK_LOGON_GROUP</b>)</li>
</ul>
All other triggers are delayed until battery saver is off. For more information about accessing battery saver status in your application, see <a href="https://msdn.microsoft.com/4c331239-4222-4650-a0ed-6d605bf376cd">SYSTEM_POWER_STATUS</a>. For general information about battery saver, see <a href="https://msdn.microsoft.com/FA82ED38-9645-45F0-98A0-B59BEE81B2A2">battery saver (in the hardware component guidelines)</a>. 




## -see-also




<a href="https://msdn.microsoft.com/7aa22af2-7f0a-41c1-89c6-d813780e89bf">IPrincipal</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

