---
UID: NN:taskschd.ITaskSettings
title: ITaskSettings
author: windows-sdk-content
description: Provides the settings that the Task Scheduler service uses to perform the task.
old-location: taskschd\itasksettings.htm
tech.root: taskschd
ms.assetid: 203264d1-f67c-45ba-931b-206d7f57a2a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITaskSettings, ITaskSettings interface [Task Scheduler], ITaskSettings interface [Task Scheduler],described, taskschd.itasksettings, taskschd/ITaskSettings
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskSettings interface


## -description


 Provides the settings that the Task Scheduler service uses to perform the task.


## -remarks



By default, a task will be stopped 72 hours after it starts to run.  You can change this by changing the <a href="https://msdn.microsoft.com/33e70133-9dfe-402a-9a1a-87f3fcc3eb96">ExecutionTimeLimit</a> setting.

When reading or writing XML for a task, the task settings are defined in the  <a href="https://msdn.microsoft.com/72d2929a-0dd2-44cd-be7b-72eca23a5e14">Settings</a> element of the Task Scheduler schema.

When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:

<ul>
<li>Not set to <b>Start the task only if the computer is idle...</b> (task doesn't use <a href="https://msdn.microsoft.com/d3bec139-f395-4658-b8be-79b7281c4f93">IdleSettings</a>)</li>
<li>Not set to run during automatic maintenance (task doesn't use <a href="https://msdn.microsoft.com/F4B6ED81-DE9A-42C8-8F16-D5BD93743CB3">MaintenanceSettings</a>)</li>
<li>Is set to <b>Run only when user is logged on</b> (task <a href="https://msdn.microsoft.com/cf0a8ad4-f1bb-46a2-ae92-d00e08b8d459">LogonType</a> is <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or <b>TASK_LOGON_GROUP</b>)</li>
</ul>
All other triggers are delayed until battery saver is off. For more information about accessing battery saver status in your application, see <a href="https://msdn.microsoft.com/4c331239-4222-4650-a0ed-6d605bf376cd">SYSTEM_POWER_STATUS</a>. For general information about battery saver, see <a href="https://msdn.microsoft.com/FA82ED38-9645-45F0-98A0-B59BEE81B2A2">battery saver (in the hardware component guidelines)</a>. 


#### Examples

For more information and a code example for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>.   

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a6bd9278-b9ac-4eb3-957a-5191cee12a6f">IIdleSettings</a>



<a href="https://msdn.microsoft.com/831e1259-df2b-4b03-8336-706727fd7b14">INetworkSettings</a>



<a href="https://msdn.microsoft.com/3787ed9b-9fd0-473b-9034-ade97dc330d9">ITaskDefinition</a>
 

 

