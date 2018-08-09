---
UID: NF:taskschd.ITaskSettings.put_Hidden
title: ITaskSettings::put_Hidden
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates that the task will not be visible in the UI.
old-location: taskschd\itasksettings_hidden.htm
old-project: taskschd
ms.assetid: 05d466e4-26f8-4fde-8c7e-9e16daadc220
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Hidden property [Task Scheduler], Hidden property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],Hidden property, ITaskSettings.Hidden, ITaskSettings.put_Hidden, ITaskSettings::Hidden, ITaskSettings::get_Hidden, ITaskSettings::put_Hidden, put_Hidden, taskschd.itasksettings_hidden, taskschd/ITaskSettings::Hidden, taskschd/ITaskSettings::get_Hidden, taskschd/ITaskSettings::put_Hidden
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskSettings.Hidden
 - ITaskSettings.get_Hidden
 - ITaskSettings.put_Hidden
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings::put_Hidden


## -description


Gets or sets a Boolean value that indicates that the task will not be visible in the UI. However, administrators can override this setting through the use of a 'master switch' that makes all tasks visible in the UI.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/a08c270f-6d4e-4473-9538-c1e1e21b3b10">Hidden (settingsType)</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

