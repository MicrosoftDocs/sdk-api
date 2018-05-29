---
UID: NF:taskschd.ITaskSettings.put_RunOnlyIfIdle
title: ITaskSettings::put_RunOnlyIfIdle
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.
old-location: taskschd\itasksettings_runonlyifidle.htm
old-project: TaskSchd
ms.assetid: 2ea0b2bd-793b-427f-9177-c8d124e5ae25
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITaskSettings interface [Task Scheduler],RunOnlyIfIdle property, ITaskSettings.RunOnlyIfIdle, ITaskSettings.put_RunOnlyIfIdle, ITaskSettings::RunOnlyIfIdle, ITaskSettings::get_RunOnlyIfIdle, ITaskSettings::put_RunOnlyIfIdle, RunOnlyIfIdle property [Task Scheduler], RunOnlyIfIdle property [Task Scheduler],ITaskSettings interface, put_RunOnlyIfIdle, taskschd.itasksettings_runonlyifidle, taskschd/ITaskSettings::RunOnlyIfIdle, taskschd/ITaskSettings::get_RunOnlyIfIdle, taskschd/ITaskSettings::put_RunOnlyIfIdle
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITaskSettings.RunOnlyIfIdle
-	ITaskSettings.get_RunOnlyIfIdle
-	ITaskSettings.put_RunOnlyIfIdle
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings::put_RunOnlyIfIdle


## -description


Gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.

This property is read/write.


## -parameters


## -remarks



When reading or writing  XML for a task, this setting is specified in the  <a href="https://msdn.microsoft.com/2ef3dd19-4d5c-4399-89b8-d737be4ef85e">RunOnlyIfIdle</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

