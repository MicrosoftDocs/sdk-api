---
UID: NF:taskschd.ITaskSettings2.get_UseUnifiedSchedulingEngine
title: ITaskSettings2::get_UseUnifiedSchedulingEngine (taskschd.h)
description: Gets or sets a Boolean value that indicates that the Unified Scheduling Engine will be utilized to run this task. (Get)
helpviewer_keywords: ["ITaskSettings2 interface [Task Scheduler]","UseUnifiedSchedulingEngine property","ITaskSettings2.UseUnifiedSchedulingEngine","ITaskSettings2.get_UseUnifiedSchedulingEngine","ITaskSettings2::UseUnifiedSchedulingEngine","ITaskSettings2::get_UseUnifiedSchedulingEngine","ITaskSettings2::put_UseUnifiedSchedulingEngine","UseUnifiedSchedulingEngine property [Task Scheduler]","UseUnifiedSchedulingEngine property [Task Scheduler]","ITaskSettings2 interface","get_UseUnifiedSchedulingEngine","taskschd.itasksettings2_useunifiedschedulingengine","taskschd/ITaskSettings2::UseUnifiedSchedulingEngine","taskschd/ITaskSettings2::get_UseUnifiedSchedulingEngine","taskschd/ITaskSettings2::put_UseUnifiedSchedulingEngine"]
old-location: taskschd\itasksettings2_useunifiedschedulingengine.htm
tech.root: taskschd
ms.assetid: bc632e8d-e53f-48c0-88cf-294451130752
ms.date: 12/05/2018
ms.keywords: ITaskSettings2 interface [Task Scheduler],UseUnifiedSchedulingEngine property, ITaskSettings2.UseUnifiedSchedulingEngine, ITaskSettings2.get_UseUnifiedSchedulingEngine, ITaskSettings2::UseUnifiedSchedulingEngine, ITaskSettings2::get_UseUnifiedSchedulingEngine, ITaskSettings2::put_UseUnifiedSchedulingEngine, UseUnifiedSchedulingEngine property [Task Scheduler], UseUnifiedSchedulingEngine property [Task Scheduler],ITaskSettings2 interface, get_UseUnifiedSchedulingEngine, taskschd.itasksettings2_useunifiedschedulingengine, taskschd/ITaskSettings2::UseUnifiedSchedulingEngine, taskschd/ITaskSettings2::get_UseUnifiedSchedulingEngine, taskschd/ITaskSettings2::put_UseUnifiedSchedulingEngine
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Taskschd.idl
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
 - ITaskSettings2::get_UseUnifiedSchedulingEngine
 - taskschd/ITaskSettings2::get_UseUnifiedSchedulingEngine
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
 - ITaskSettings2.UseUnifiedSchedulingEngine
 - ITaskSettings2.get_UseUnifiedSchedulingEngine
 - ITaskSettings2.put_UseUnifiedSchedulingEngine
---

# ITaskSettings2::get_UseUnifiedSchedulingEngine


## -description

Gets or sets a Boolean value that indicates that the Unified Scheduling Engine will be utilized to run this task.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-useunifiedschedulingengine-settingstype-element">UseUnifiedSchedulingEngine</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings2">ITaskSettings2</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
