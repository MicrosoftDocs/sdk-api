---
UID: NF:taskschd.ITaskSettings.put_RestartInterval
title: ITaskSettings::put_RestartInterval
author: windows-sdk-content
description: Gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.
old-location: taskschd\itasksettings_restartinterval.htm
old-project: taskschd
ms.assetid: 6fe72035-e5f3-4c87-9dce-ba07374e7086
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITaskSettings interface [Task Scheduler],RestartInterval property, ITaskSettings.RestartInterval, ITaskSettings.put_RestartInterval, ITaskSettings::RestartInterval, ITaskSettings::get_RestartInterval, ITaskSettings::put_RestartInterval, RestartInterval property [Task Scheduler], RestartInterval property [Task Scheduler],ITaskSettings interface, put_RestartInterval, taskschd.itasksettings_restartinterval, taskschd/ITaskSettings::RestartInterval, taskschd/ITaskSettings::get_RestartInterval, taskschd/ITaskSettings::put_RestartInterval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.redist: 
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings::put_RestartInterval


## -description


Gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1">Interval</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

