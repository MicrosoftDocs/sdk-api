---
UID: NF:taskschd.ITaskSettings.get_AllowDemandStart
title: ITaskSettings::get_AllowDemandStart (taskschd.h)
description: Gets or sets a Boolean value that indicates that the task can be started by using either the Run command or the Context menu. (Get)
helpviewer_keywords: ["AllowDemandStart property [Task Scheduler]","AllowDemandStart property [Task Scheduler]","ITaskSettings interface","ITaskSettings interface [Task Scheduler]","AllowDemandStart property","ITaskSettings.AllowDemandStart","ITaskSettings.get_AllowDemandStart","ITaskSettings::AllowDemandStart","ITaskSettings::get_AllowDemandStart","ITaskSettings::put_AllowDemandStart","get_AllowDemandStart","taskschd.itasksettings_allowdemandstart","taskschd/ITaskSettings::AllowDemandStart","taskschd/ITaskSettings::get_AllowDemandStart","taskschd/ITaskSettings::put_AllowDemandStart"]
old-location: taskschd\itasksettings_allowdemandstart.htm
tech.root: taskschd
ms.assetid: 267cf3c3-0e18-4a4f-bb32-d6766ceb6241
ms.date: 12/05/2018
ms.keywords: AllowDemandStart property [Task Scheduler], AllowDemandStart property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],AllowDemandStart property, ITaskSettings.AllowDemandStart, ITaskSettings.get_AllowDemandStart, ITaskSettings::AllowDemandStart, ITaskSettings::get_AllowDemandStart, ITaskSettings::put_AllowDemandStart, get_AllowDemandStart, taskschd.itasksettings_allowdemandstart, taskschd/ITaskSettings::AllowDemandStart, taskschd/ITaskSettings::get_AllowDemandStart, taskschd/ITaskSettings::put_AllowDemandStart
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskSettings::get_AllowDemandStart
 - taskschd/ITaskSettings::get_AllowDemandStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskSettings.AllowDemandStart
 - ITaskSettings.get_AllowDemandStart
 - ITaskSettings.put_AllowDemandStart
---

# ITaskSettings::get_AllowDemandStart


## -description

Gets or sets  a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.

This property is read/write.

## -parameters

## -remarks

When this property is set to True, the task can be started independent of when any triggers start the task.

When reading or writing  XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-allowstartondemand-settingstype-element">AllowStartOnDemand</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
