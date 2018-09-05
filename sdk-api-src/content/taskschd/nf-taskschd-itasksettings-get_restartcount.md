---
UID: NF:taskschd.ITaskSettings.get_RestartCount
title: ITaskSettings::get_RestartCount
author: windows-sdk-content
description: Gets or sets the number of times that the Task Scheduler will attempt to restart the task.
old-location: taskschd\itasksettings_restartcount.htm
old-project: TaskSchd
ms.assetid: ec77a7bf-52d8-4f0f-ab47-f0555b666a70
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ITaskSettings interface [Task Scheduler],RestartCount property, ITaskSettings.RestartCount, ITaskSettings.get_RestartCount, ITaskSettings::RestartCount, ITaskSettings::get_RestartCount, ITaskSettings::put_RestartCount, RestartCount property [Task Scheduler], RestartCount property [Task Scheduler],ITaskSettings interface, get_RestartCount, taskschd.itasksettings_restartcount, taskschd/ITaskSettings::RestartCount, taskschd/ITaskSettings::get_RestartCount, taskschd/ITaskSettings::put_RestartCount
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
 - ITaskSettings.RestartCount
 - ITaskSettings.get_RestartCount
 - ITaskSettings.put_RestartCount
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings::get_RestartCount


## -description


Gets or sets the number of times that the Task Scheduler will attempt to restart the task.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/67466c14-c9dd-49c8-a6ed-df7531fc63b8">Count</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

