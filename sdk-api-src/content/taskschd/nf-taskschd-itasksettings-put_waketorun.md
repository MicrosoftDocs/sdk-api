---
UID: NF:taskschd.ITaskSettings.put_WakeToRun
title: ITaskSettings::put_WakeToRun (taskschd.h)
description: Gets or sets a Boolean value that indicates that the Task Scheduler will wake the computer when it is time to run the task, and keep the computer awake until the task is completed.
old-location: taskschd\itasksettings_waketorun.htm
tech.root: taskschd
ms.assetid: efa1c7cd-7a70-4760-909f-bb5a1ede35f4
ms.date: 12/05/2018
ms.keywords: ITaskSettings interface [Task Scheduler],WakeToRun property, ITaskSettings.WakeToRun, ITaskSettings.put_WakeToRun, ITaskSettings::WakeToRun, ITaskSettings::get_WakeToRun, ITaskSettings::put_WakeToRun, WakeToRun property [Task Scheduler], WakeToRun property [Task Scheduler],ITaskSettings interface, put_WakeToRun, taskschd.itasksettings_waketorun, taskschd/ITaskSettings::WakeToRun, taskschd/ITaskSettings::get_WakeToRun, taskschd/ITaskSettings::put_WakeToRun
ms.topic: method
f1_keywords:
- taskschd/ITaskSettings.WakeToRun
dev_langs:
- c++
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
- ITaskSettings.WakeToRun
- ITaskSettings.get_WakeToRun
- ITaskSettings.put_WakeToRun
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskSettings::put_WakeToRun


## -description


Gets or sets a Boolean value that indicates that the Task Scheduler will wake the computer when it is time to run the task, and keep the computer awake until the task is completed.

This property is read/write.


## -parameters


## -remarks



If a task has this property set to true, and is triggered when the computer is already awake, Task Scheduler will request the computer to stay awake until the task has completed running.

When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode. The screen will turn on when Windows Vista detects that a user has returned to use the computer.

When reading or writing  XML for a task, this setting is specified in the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-waketorun-settingstype-element">WakeToRun</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

