---
UID: NF:taskschd.ITaskSettings.get_IdleSettings
title: ITaskSettings::get_IdleSettings method
author: windows-driver-content
description: Gets or sets the information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.
old-location: taskschd\itasksettings_idlesettings.htm
old-project: TaskSchd
ms.assetid: d3bec139-f395-4658-b8be-79b7281c4f93
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ITaskSettings, ITaskSettings interface [Task Scheduler], IdleSettings property, ITaskSettings.IdleSettings, ITaskSettings::get_IdleSettings, ITaskSettings::put_IdleSettings, IdleSettings property [Task Scheduler], IdleSettings property [Task Scheduler], ITaskSettings interface, get_IdleSettings,ITaskSettings.get_IdleSettings, taskschd.itasksettings_idlesettings, taskschd/ITaskSettings::IdleSettings, taskschd/ITaskSettings::get_IdleSettings, taskschd/ITaskSettings::put_IdleSettings
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITaskSettings.IdleSettings
-	ITaskSettings.get_IdleSettings
-	ITaskSettings.put_IdleSettings
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings::get_IdleSettings method


## -description


Gets or sets the  information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition. For information about idle conditions, see <a href="https://msdn.microsoft.com/1e480681-b77a-48fe-a732-dd1591eaa08d">Task Idle Conditions</a>.

This property is read/write.


## -parameters


## -remarks



When reading or writing  XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/23d57417-95a9-42e3-904c-7f0859fcda7c">IdleSettings</a> element of the Task Scheduler schema.

When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:

<ul>
<li>Not set to <b>Start the task only if the computer is idle...</b> (task doesn't use <b>IdleSettings</b>)</li>
<li>Not set to run during automatic maintenance (task doesn't use <a href="https://msdn.microsoft.com/F4B6ED81-DE9A-42C8-8F16-D5BD93743CB3">MaintenanceSettings</a>)</li>
<li>Is set to <b>Run only when user is logged on</b> (task <a href="https://msdn.microsoft.com/cf0a8ad4-f1bb-46a2-ae92-d00e08b8d459">LogonType</a> is <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or <b>TASK_LOGON_GROUP</b>)</li>
</ul>
All other triggers are delayed until battery saver is off. For more information about accessing battery saver status in your application, see <a href="https://msdn.microsoft.com/4c331239-4222-4650-a0ed-6d605bf376cd">SYSTEM_POWER_STATUS</a>. For general information about battery saver, see <a href="https://msdn.microsoft.com/FA82ED38-9645-45F0-98A0-B59BEE81B2A2">battery saver (in the hardware component guidelines)</a>. 




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

