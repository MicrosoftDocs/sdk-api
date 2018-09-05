---
UID: NF:taskschd.ITaskSettings.get_DisallowStartIfOnBatteries
title: ITaskSettings::get_DisallowStartIfOnBatteries
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.
old-location: taskschd\itasksettings_disallowstartifonbatteries.htm
old-project: TaskSchd
ms.assetid: 8f80bc2a-8b7d-4771-b773-55b8f50a4126
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DisallowStartIfOnBatteries property [Task Scheduler], DisallowStartIfOnBatteries property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],DisallowStartIfOnBatteries property, ITaskSettings.DisallowStartIfOnBatteries, ITaskSettings.get_DisallowStartIfOnBatteries, ITaskSettings::DisallowStartIfOnBatteries, ITaskSettings::get_DisallowStartIfOnBatteries, ITaskSettings::put_DisallowStartIfOnBatteries, get_DisallowStartIfOnBatteries, taskschd.itasksettings_disallowstartifonbatteries, taskschd/ITaskSettings::DisallowStartIfOnBatteries, taskschd/ITaskSettings::get_DisallowStartIfOnBatteries, taskschd/ITaskSettings::put_DisallowStartIfOnBatteries
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
 - ITaskSettings.DisallowStartIfOnBatteries
 - ITaskSettings.get_DisallowStartIfOnBatteries
 - ITaskSettings.put_DisallowStartIfOnBatteries
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings::get_DisallowStartIfOnBatteries


## -description


Gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/48c0fd32-4441-4628-8090-c736f2945b4d">DisallowStartIfOnBatteries</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

