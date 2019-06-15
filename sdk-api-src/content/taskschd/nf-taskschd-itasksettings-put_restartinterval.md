---
UID: NF:taskschd.ITaskSettings.put_RestartInterval
title: ITaskSettings::put_RestartInterval (taskschd.h)
author: windows-sdk-content
description: Gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.
old-location: taskschd\itasksettings_restartinterval.htm
tech.root: taskschd
ms.assetid: 6fe72035-e5f3-4c87-9dce-ba07374e7086
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITaskSettings interface [Task Scheduler],RestartInterval property, ITaskSettings.RestartInterval, ITaskSettings.put_RestartInterval, ITaskSettings::RestartInterval, ITaskSettings::get_RestartInterval, ITaskSettings::put_RestartInterval, RestartInterval property [Task Scheduler], RestartInterval property [Task Scheduler],ITaskSettings interface, put_RestartInterval, taskschd.itasksettings_restartinterval, taskschd/ITaskSettings::RestartInterval, taskschd/ITaskSettings::get_RestartInterval, taskschd/ITaskSettings::put_RestartInterval
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
 - ITaskSettings.RestartInterval
 - ITaskSettings.get_RestartInterval
 - ITaskSettings.put_RestartInterval
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskSettings::put_RestartInterval


## -description


Gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-interval-restarttype-element">Interval</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

