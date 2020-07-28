---
UID: NF:taskschd.ITaskSettings.get_RunOnlyIfIdle
title: ITaskSettings::get_RunOnlyIfIdle (taskschd.h)
description: Gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.
helpviewer_keywords: ["ITaskSettings interface [Task Scheduler]","RunOnlyIfIdle property","ITaskSettings.RunOnlyIfIdle","ITaskSettings.get_RunOnlyIfIdle","ITaskSettings::RunOnlyIfIdle","ITaskSettings::get_RunOnlyIfIdle","ITaskSettings::put_RunOnlyIfIdle","RunOnlyIfIdle property [Task Scheduler]","RunOnlyIfIdle property [Task Scheduler]","ITaskSettings interface","get_RunOnlyIfIdle","taskschd.itasksettings_runonlyifidle","taskschd/ITaskSettings::RunOnlyIfIdle","taskschd/ITaskSettings::get_RunOnlyIfIdle","taskschd/ITaskSettings::put_RunOnlyIfIdle"]
old-location: taskschd\itasksettings_runonlyifidle.htm
tech.root: taskschd
ms.assetid: 2ea0b2bd-793b-427f-9177-c8d124e5ae25
ms.date: 12/05/2018
ms.keywords: ITaskSettings interface [Task Scheduler],RunOnlyIfIdle property, ITaskSettings.RunOnlyIfIdle, ITaskSettings.get_RunOnlyIfIdle, ITaskSettings::RunOnlyIfIdle, ITaskSettings::get_RunOnlyIfIdle, ITaskSettings::put_RunOnlyIfIdle, RunOnlyIfIdle property [Task Scheduler], RunOnlyIfIdle property [Task Scheduler],ITaskSettings interface, get_RunOnlyIfIdle, taskschd.itasksettings_runonlyifidle, taskschd/ITaskSettings::RunOnlyIfIdle, taskschd/ITaskSettings::get_RunOnlyIfIdle, taskschd/ITaskSettings::put_RunOnlyIfIdle
f1_keywords:
- taskschd/ITaskSettings.RunOnlyIfIdle
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
- ITaskSettings.RunOnlyIfIdle
- ITaskSettings.get_RunOnlyIfIdle
- ITaskSettings.put_RunOnlyIfIdle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskSettings::get_RunOnlyIfIdle


## -description


Gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.

This property is read/write.


## -parameters


## -remarks



When reading or writing  XML for a task, this setting is specified in the  <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-runonlyifidle-settingstype-element">RunOnlyIfIdle</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

