---
UID: NF:taskschd.ITaskSettings.get_Enabled
title: ITaskSettings::get_Enabled (taskschd.h)
description: Gets or sets a Boolean value that indicates that the task is enabled. The task can be performed only when this setting is True.
helpviewer_keywords: ["Enabled property [Task Scheduler]","Enabled property [Task Scheduler]","ITaskSettings interface","ITaskSettings interface [Task Scheduler]","Enabled property","ITaskSettings.Enabled","ITaskSettings.get_Enabled","ITaskSettings::Enabled","ITaskSettings::get_Enabled","get_Enabled","taskschd.itasksettings_enabled","taskschd/ITaskSettings::Enabled","taskschd/ITaskSettings::get_Enabled"]
old-location: taskschd\itasksettings_enabled.htm
tech.root: taskschd
ms.assetid: 6c6e7f51-9591-4b84-b06b-124cd88a0345
ms.date: 12/05/2018
ms.keywords: Enabled property [Task Scheduler], Enabled property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],Enabled property, ITaskSettings.Enabled, ITaskSettings.get_Enabled, ITaskSettings::Enabled, ITaskSettings::get_Enabled, get_Enabled, taskschd.itasksettings_enabled, taskschd/ITaskSettings::Enabled, taskschd/ITaskSettings::get_Enabled
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
 - ITaskSettings::get_Enabled
 - taskschd/ITaskSettings::get_Enabled
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
 - ITaskSettings.Enabled
 - ITaskSettings.get_Enabled
---

# ITaskSettings::get_Enabled


## -description

Gets or sets a Boolean value that indicates that the task is enabled. The task can be performed only when this setting is True.

This property is read-only.

## -parameters

## -remarks

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-enabled-settingstype-element">Enabled (settingsType)</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>