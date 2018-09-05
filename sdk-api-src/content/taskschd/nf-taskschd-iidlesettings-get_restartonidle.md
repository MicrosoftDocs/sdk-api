---
UID: NF:taskschd.IIdleSettings.get_RestartOnIdle
title: IIdleSettings::get_RestartOnIdle
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.
old-location: taskschd\iidlesettings_restartonidle.htm
old-project: TaskSchd
ms.assetid: 42779c7d-4739-47c5-bf35-5d6c612c59c0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IIdleSettings interface [Task Scheduler],RestartOnIdle property, IIdleSettings.RestartOnIdle, IIdleSettings.get_RestartOnIdle, IIdleSettings::RestartOnIdle, IIdleSettings::get_RestartOnIdle, IIdleSettings::put_RestartOnIdle, RestartOnIdle property [Task Scheduler], RestartOnIdle property [Task Scheduler],IIdleSettings interface, get_RestartOnIdle, taskschd.iidlesettings_restartonidle, taskschd/IIdleSettings::RestartOnIdle, taskschd/IIdleSettings::get_RestartOnIdle, taskschd/IIdleSettings::put_RestartOnIdle
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
 - IIdleSettings.RestartOnIdle
 - IIdleSettings.get_RestartOnIdle
 - IIdleSettings.put_RestartOnIdle
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IIdleSettings::get_RestartOnIdle


## -description


Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.

This property is read/write.


## -parameters


## -remarks



This property is only used if the <a href="https://msdn.microsoft.com/0799194f-dd3d-4aa6-b17b-0abe933f9b55">StopOnIdleEnd</a> property is set to True.

When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/7a7a388c-8dc9-4106-82c1-3435d9f89866">RestartOnIdle</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/a6bd9278-b9ac-4eb3-957a-5191cee12a6f">IIdleSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

