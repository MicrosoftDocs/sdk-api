---
UID: NF:taskschd.ITaskSettings3.put_MaintenanceSettings
title: ITaskSettings3::put_MaintenanceSettings (taskschd.h)
author: windows-sdk-content
description: Gets or sets a pointer to pointer to an IMaintenanceSettingsobject that Task scheduler uses to perform a task during Automatic maintenance.
old-location: taskschd\itasksettings3_maintenancesettings.htm
tech.root: taskschd
ms.assetid: F4B6ED81-DE9A-42C8-8F16-D5BD93743CB3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITaskSettings3 interface [Task Scheduler],MaintenanceSettings property, ITaskSettings3.MaintenanceSettings, ITaskSettings3.put_MaintenanceSettings, ITaskSettings3::MaintenanceSettings, ITaskSettings3::get_MaintenanceSettings, ITaskSettings3::put_MaintenanceSettings, MaintenanceSettings property [Task Scheduler], MaintenanceSettings property [Task Scheduler],ITaskSettings3 interface, put_MaintenanceSettings, taskschd.itasksettings3_maintenancesettings, taskschd/ITaskSettings3::MaintenanceSettings, taskschd/ITaskSettings3::get_MaintenanceSettings, taskschd/ITaskSettings3::put_MaintenanceSettings
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Taskschd.idl
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
 - Taskschd.dll
api_name:
 - ITaskSettings3.MaintenanceSettings
 - ITaskSettings3.get_MaintenanceSettings
 - ITaskSettings3.put_MaintenanceSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskSettings3::put_MaintenanceSettings


## -description


Gets or sets a pointer to pointer to an <a href="https://msdn.microsoft.com/5AB172CA-66BF-47B8-952A-9CBA13A20668">IMaintenanceSettings</a>object that Task scheduler uses to perform a task during Automatic maintenance.

This property is read/write.


## -parameters


## -remarks



When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:

<ul>
<li>Not set to <b>Start the task only if the computer is idle...</b> (task doesn't use <a href="https://msdn.microsoft.com/d3bec139-f395-4658-b8be-79b7281c4f93">IdleSettings</a>)</li>
<li>Not set to run during automatic maintenance (task doesn't use <b>MaintenanceSettings</b>)</li>
<li>Is set to <b>Run only when user is logged on</b> (task <a href="https://msdn.microsoft.com/cf0a8ad4-f1bb-46a2-ae92-d00e08b8d459">LogonType</a> is <b>TASK_LOGON_INTERACTIVE_TOKEN</b> or <b>TASK_LOGON_GROUP</b>)</li>
</ul>
All other triggers are delayed until battery saver is off. For more information about accessing battery saver status in your application, see <a href="https://msdn.microsoft.com/4c331239-4222-4650-a0ed-6d605bf376cd">SYSTEM_POWER_STATUS</a>. For general information about battery saver, see <a href="https://msdn.microsoft.com/FA82ED38-9645-45F0-98A0-B59BEE81B2A2">battery saver (in the hardware component guidelines)</a>. 




## -see-also




<a href="https://msdn.microsoft.com/B0315585-A41C-423C-A059-14C2F04F6652">ITaskSettings3</a>
 

 

