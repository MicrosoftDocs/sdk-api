---
UID: NF:taskschd.ITaskSettings.put_MultipleInstances
title: ITaskSettings::put_MultipleInstances (taskschd.h)
description: Gets or sets the policy that defines how the Task Scheduler deals with multiple instances of the task. (Put)
helpviewer_keywords: ["ITaskSettings interface [Task Scheduler]","MultipleInstances property","ITaskSettings.MultipleInstances","ITaskSettings.put_MultipleInstances","ITaskSettings::MultipleInstances","ITaskSettings::get_MultipleInstances","ITaskSettings::put_MultipleInstances","MultipleInstances property [Task Scheduler]","MultipleInstances property [Task Scheduler]","ITaskSettings interface","TASK_INSTANCES_IGNORE_NEW","TASK_INSTANCES_PARALLEL","TASK_INSTANCES_QUEUE","TASK_INSTANCES_STOP_EXISTING","put_MultipleInstances","taskschd.itasksettings_multipleinstances","taskschd/ITaskSettings::MultipleInstances","taskschd/ITaskSettings::get_MultipleInstances","taskschd/ITaskSettings::put_MultipleInstances"]
old-location: taskschd\itasksettings_multipleinstances.htm
tech.root: taskschd
ms.assetid: 2a84b780-2378-4ee8-aaa4-3bc960e32206
ms.date: 12/05/2018
ms.keywords: ITaskSettings interface [Task Scheduler],MultipleInstances property, ITaskSettings.MultipleInstances, ITaskSettings.put_MultipleInstances, ITaskSettings::MultipleInstances, ITaskSettings::get_MultipleInstances, ITaskSettings::put_MultipleInstances, MultipleInstances property [Task Scheduler], MultipleInstances property [Task Scheduler],ITaskSettings interface, TASK_INSTANCES_IGNORE_NEW, TASK_INSTANCES_PARALLEL, TASK_INSTANCES_QUEUE, TASK_INSTANCES_STOP_EXISTING, put_MultipleInstances, taskschd.itasksettings_multipleinstances, taskschd/ITaskSettings::MultipleInstances, taskschd/ITaskSettings::get_MultipleInstances, taskschd/ITaskSettings::put_MultipleInstances
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
 - ITaskSettings::put_MultipleInstances
 - taskschd/ITaskSettings::put_MultipleInstances
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
 - ITaskSettings.MultipleInstances
 - ITaskSettings.get_MultipleInstances
 - ITaskSettings.put_MultipleInstances
---

# ITaskSettings::put_MultipleInstances


## -description

Gets or sets the policy that defines how the Task Scheduler deals with multiple instances of the task.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-multipleinstancespolicy-settingstype-element">MultipleInstancesPolicy</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy">TASK_INSTANCES_POLICY</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
