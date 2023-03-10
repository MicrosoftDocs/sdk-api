---
UID: NF:taskschd.ITaskSettings.put_DisallowStartIfOnBatteries
title: ITaskSettings::put_DisallowStartIfOnBatteries (taskschd.h)
description: Gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries. (Put)
helpviewer_keywords: ["DisallowStartIfOnBatteries property [Task Scheduler]","DisallowStartIfOnBatteries property [Task Scheduler]","ITaskSettings interface","ITaskSettings interface [Task Scheduler]","DisallowStartIfOnBatteries property","ITaskSettings.DisallowStartIfOnBatteries","ITaskSettings.put_DisallowStartIfOnBatteries","ITaskSettings::DisallowStartIfOnBatteries","ITaskSettings::get_DisallowStartIfOnBatteries","ITaskSettings::put_DisallowStartIfOnBatteries","put_DisallowStartIfOnBatteries","taskschd.itasksettings_disallowstartifonbatteries","taskschd/ITaskSettings::DisallowStartIfOnBatteries","taskschd/ITaskSettings::get_DisallowStartIfOnBatteries","taskschd/ITaskSettings::put_DisallowStartIfOnBatteries"]
old-location: taskschd\itasksettings_disallowstartifonbatteries.htm
tech.root: taskschd
ms.assetid: 8f80bc2a-8b7d-4771-b773-55b8f50a4126
ms.date: 12/05/2018
ms.keywords: DisallowStartIfOnBatteries property [Task Scheduler], DisallowStartIfOnBatteries property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],DisallowStartIfOnBatteries property, ITaskSettings.DisallowStartIfOnBatteries, ITaskSettings.put_DisallowStartIfOnBatteries, ITaskSettings::DisallowStartIfOnBatteries, ITaskSettings::get_DisallowStartIfOnBatteries, ITaskSettings::put_DisallowStartIfOnBatteries, put_DisallowStartIfOnBatteries, taskschd.itasksettings_disallowstartifonbatteries, taskschd/ITaskSettings::DisallowStartIfOnBatteries, taskschd/ITaskSettings::get_DisallowStartIfOnBatteries, taskschd/ITaskSettings::put_DisallowStartIfOnBatteries
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
 - ITaskSettings::put_DisallowStartIfOnBatteries
 - taskschd/ITaskSettings::put_DisallowStartIfOnBatteries
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
 - ITaskSettings.DisallowStartIfOnBatteries
 - ITaskSettings.get_DisallowStartIfOnBatteries
 - ITaskSettings.put_DisallowStartIfOnBatteries
---

# ITaskSettings::put_DisallowStartIfOnBatteries


## -description

Gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-disallowstartifonbatteries-settingstype-element">DisallowStartIfOnBatteries</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
