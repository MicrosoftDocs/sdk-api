---
UID: NF:taskschd.ITaskSettings.get_RestartCount
title: ITaskSettings::get_RestartCount (taskschd.h)
description: Gets or sets the number of times that the Task Scheduler will attempt to restart the task. (Get)
helpviewer_keywords: ["ITaskSettings interface [Task Scheduler]","RestartCount property","ITaskSettings.RestartCount","ITaskSettings.get_RestartCount","ITaskSettings::RestartCount","ITaskSettings::get_RestartCount","ITaskSettings::put_RestartCount","RestartCount property [Task Scheduler]","RestartCount property [Task Scheduler]","ITaskSettings interface","get_RestartCount","taskschd.itasksettings_restartcount","taskschd/ITaskSettings::RestartCount","taskschd/ITaskSettings::get_RestartCount","taskschd/ITaskSettings::put_RestartCount"]
old-location: taskschd\itasksettings_restartcount.htm
tech.root: taskschd
ms.assetid: ec77a7bf-52d8-4f0f-ab47-f0555b666a70
ms.date: 12/05/2018
ms.keywords: ITaskSettings interface [Task Scheduler],RestartCount property, ITaskSettings.RestartCount, ITaskSettings.get_RestartCount, ITaskSettings::RestartCount, ITaskSettings::get_RestartCount, ITaskSettings::put_RestartCount, RestartCount property [Task Scheduler], RestartCount property [Task Scheduler],ITaskSettings interface, get_RestartCount, taskschd.itasksettings_restartcount, taskschd/ITaskSettings::RestartCount, taskschd/ITaskSettings::get_RestartCount, taskschd/ITaskSettings::put_RestartCount
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
 - ITaskSettings::get_RestartCount
 - taskschd/ITaskSettings::get_RestartCount
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
 - ITaskSettings.RestartCount
 - ITaskSettings.get_RestartCount
 - ITaskSettings.put_RestartCount
---

# ITaskSettings::get_RestartCount


## -description

Gets or sets the number of times that the Task Scheduler will attempt to restart the task.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-count-restarttype-element">Count</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
