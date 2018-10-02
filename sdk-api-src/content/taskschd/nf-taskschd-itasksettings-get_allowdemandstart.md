---
UID: NF:taskschd.ITaskSettings.get_AllowDemandStart
title: ITaskSettings::get_AllowDemandStart
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.
old-location: taskschd\itasksettings_allowdemandstart.htm
tech.root: TaskSchd
ms.assetid: 267cf3c3-0e18-4a4f-bb32-d6766ceb6241
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AllowDemandStart property [Task Scheduler], AllowDemandStart property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],AllowDemandStart property, ITaskSettings.AllowDemandStart, ITaskSettings.get_AllowDemandStart, ITaskSettings::AllowDemandStart, ITaskSettings::get_AllowDemandStart, ITaskSettings::put_AllowDemandStart, get_AllowDemandStart, taskschd.itasksettings_allowdemandstart, taskschd/ITaskSettings::AllowDemandStart, taskschd/ITaskSettings::get_AllowDemandStart, taskschd/ITaskSettings::put_AllowDemandStart
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
 - ITaskSettings.AllowDemandStart
 - ITaskSettings.get_AllowDemandStart
 - ITaskSettings.put_AllowDemandStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskSettings::get_AllowDemandStart


## -description


Gets or sets  a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.

This property is read/write.


## -parameters


## -remarks



When this property is set to True, the task can be started independent of when any triggers start the task.

When reading or writing  XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/5a0f0842-9f09-4d52-bed2-45740945d9a5">AllowStartOnDemand</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

