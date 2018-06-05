---
UID: NF:taskschd.ITaskSettings.get_StopIfGoingOnBatteries
title: ITaskSettings::get_StopIfGoingOnBatteries
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.
old-location: taskschd\itasksettings_stopifgoingonbatteries.htm
old-project: TaskSchd
ms.assetid: 84647124-8cb2-47f9-a86c-80bb2a629c88
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITaskSettings interface [Task Scheduler],StopIfGoingOnBatteries property, ITaskSettings.StopIfGoingOnBatteries, ITaskSettings.get_StopIfGoingOnBatteries, ITaskSettings::StopIfGoingOnBatteries, ITaskSettings::get_StopIfGoingOnBatteries, ITaskSettings::put_StopIfGoingOnBatteries, StopIfGoingOnBatteries property [Task Scheduler], StopIfGoingOnBatteries property [Task Scheduler],ITaskSettings interface, get_StopIfGoingOnBatteries, taskschd.itasksettings_stopifgoingonbatteries, taskschd/ITaskSettings::StopIfGoingOnBatteries, taskschd/ITaskSettings::get_StopIfGoingOnBatteries, taskschd/ITaskSettings::put_StopIfGoingOnBatteries
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITaskSettings.StopIfGoingOnBatteries
-	ITaskSettings.get_StopIfGoingOnBatteries
-	ITaskSettings.put_StopIfGoingOnBatteries
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings::get_StopIfGoingOnBatteries


## -description


Gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/0d772dbb-a552-45ed-9dc0-7159f6ef12ed">StopIfGoingOnBatteries</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

