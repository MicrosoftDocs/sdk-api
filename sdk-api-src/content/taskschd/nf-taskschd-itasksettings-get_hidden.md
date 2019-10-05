---
UID: NF:taskschd.ITaskSettings.get_Hidden
title: ITaskSettings::get_Hidden (taskschd.h)
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates that the task will not be visible in the UI.
old-location: taskschd\itasksettings_hidden.htm
tech.root: taskschd
ms.assetid: 05d466e4-26f8-4fde-8c7e-9e16daadc220
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Hidden property [Task Scheduler], Hidden property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],Hidden property, ITaskSettings.Hidden, ITaskSettings.get_Hidden, ITaskSettings::Hidden, ITaskSettings::get_Hidden, ITaskSettings::put_Hidden, get_Hidden, taskschd.itasksettings_hidden, taskschd/ITaskSettings::Hidden, taskschd/ITaskSettings::get_Hidden, taskschd/ITaskSettings::put_Hidden
ms.topic: method
f1_keywords: 
 - "taskschd/ITaskSettings.Hidden"
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
 - ITaskSettings.Hidden
 - ITaskSettings.get_Hidden
 - ITaskSettings.put_Hidden
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskSettings::get_Hidden


## -description


Gets or sets a Boolean value that indicates that the task will not be visible in the UI. However, administrators can override this setting through the use of a 'master switch' that makes all tasks visible in the UI.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-hidden-settingstype-element">Hidden (settingsType)</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

