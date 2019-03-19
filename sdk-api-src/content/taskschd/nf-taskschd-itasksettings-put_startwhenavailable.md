---
UID: NF:taskschd.ITaskSettings.put_StartWhenAvailable
title: ITaskSettings::put_StartWhenAvailable (taskschd.h)
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.
old-location: taskschd\itasksettings_startwhenavailable.htm
tech.root: taskschd
ms.assetid: 93002ed0-4d85-491c-9111-6bb5d62ebac2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITaskSettings interface [Task Scheduler],StartWhenAvailable property, ITaskSettings.StartWhenAvailable, ITaskSettings.put_StartWhenAvailable, ITaskSettings::StartWhenAvailable, ITaskSettings::get_StartWhenAvailable, ITaskSettings::put_StartWhenAvailable, StartWhenAvailable property [Task Scheduler], StartWhenAvailable property [Task Scheduler],ITaskSettings interface, put_StartWhenAvailable, taskschd.itasksettings_startwhenavailable, taskschd/ITaskSettings::StartWhenAvailable, taskschd/ITaskSettings::get_StartWhenAvailable, taskschd/ITaskSettings::put_StartWhenAvailable
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
 - ITaskSettings.StartWhenAvailable
 - ITaskSettings.get_StartWhenAvailable
 - ITaskSettings.put_StartWhenAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskSettings::put_StartWhenAvailable


## -description


Gets or sets a Boolean value that indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.

This property is read/write.


## -parameters


## -remarks



This property applies only to time-based tasks with an end boundary or time-based tasks that are set to repeat infinitely.

Tasks that are started after the scheduled time has passed (because of the <b>StartWhenAvailable</b> property being set to True) are queued in the Task Scheduler service's queue of tasks and they are started after a delay.  The default delay is 10 minutes.

When reading or writing  XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/1d65fd51-3a94-4083-8e38-2a652383656a">StartWhenAvailable</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

