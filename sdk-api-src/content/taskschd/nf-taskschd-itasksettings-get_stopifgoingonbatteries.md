---
UID: NF:taskschd.ITaskSettings.get_StopIfGoingOnBatteries
title: ITaskSettings::get_StopIfGoingOnBatteries (taskschd.h)
description: Gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.
helpviewer_keywords: ["ITaskSettings interface [Task Scheduler]","StopIfGoingOnBatteries property","ITaskSettings.StopIfGoingOnBatteries","ITaskSettings.get_StopIfGoingOnBatteries","ITaskSettings::StopIfGoingOnBatteries","ITaskSettings::get_StopIfGoingOnBatteries","ITaskSettings::put_StopIfGoingOnBatteries","StopIfGoingOnBatteries property [Task Scheduler]","StopIfGoingOnBatteries property [Task Scheduler]","ITaskSettings interface","get_StopIfGoingOnBatteries","taskschd.itasksettings_stopifgoingonbatteries","taskschd/ITaskSettings::StopIfGoingOnBatteries","taskschd/ITaskSettings::get_StopIfGoingOnBatteries","taskschd/ITaskSettings::put_StopIfGoingOnBatteries"]
old-location: taskschd\itasksettings_stopifgoingonbatteries.htm
tech.root: taskschd
ms.assetid: 84647124-8cb2-47f9-a86c-80bb2a629c88
ms.date: 12/05/2018
ms.keywords: ITaskSettings interface [Task Scheduler],StopIfGoingOnBatteries property, ITaskSettings.StopIfGoingOnBatteries, ITaskSettings.get_StopIfGoingOnBatteries, ITaskSettings::StopIfGoingOnBatteries, ITaskSettings::get_StopIfGoingOnBatteries, ITaskSettings::put_StopIfGoingOnBatteries, StopIfGoingOnBatteries property [Task Scheduler], StopIfGoingOnBatteries property [Task Scheduler],ITaskSettings interface, get_StopIfGoingOnBatteries, taskschd.itasksettings_stopifgoingonbatteries, taskschd/ITaskSettings::StopIfGoingOnBatteries, taskschd/ITaskSettings::get_StopIfGoingOnBatteries, taskschd/ITaskSettings::put_StopIfGoingOnBatteries
f1_keywords:
- taskschd/ITaskSettings.StopIfGoingOnBatteries
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
- ITaskSettings.StopIfGoingOnBatteries
- ITaskSettings.get_StopIfGoingOnBatteries
- ITaskSettings.put_StopIfGoingOnBatteries
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskSettings::get_StopIfGoingOnBatteries


## -description


Gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-stopifgoingonbatteries-settingstype-element">StopIfGoingOnBatteries</a> element of the Task Scheduler schema.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

