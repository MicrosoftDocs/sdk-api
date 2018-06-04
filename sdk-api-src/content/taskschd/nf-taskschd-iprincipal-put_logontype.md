---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPrincipal::put_LogonType


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
 

 

