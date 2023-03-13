---
UID: NE:taskschd._TASK_INSTANCES_POLICY
title: TASK_INSTANCES_POLICY (taskschd.h)
description: Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.
helpviewer_keywords: ["TASK_INSTANCES_IGNORE_NEW","TASK_INSTANCES_PARALLEL","TASK_INSTANCES_POLICY","TASK_INSTANCES_POLICY enumeration [Task Scheduler]","TASK_INSTANCES_QUEUE","TASK_INSTANCES_STOP_EXISTING","taskschd.task_instances_policy","taskschd/TASK_INSTANCES_IGNORE_NEW","taskschd/TASK_INSTANCES_PARALLEL","taskschd/TASK_INSTANCES_POLICY","taskschd/TASK_INSTANCES_QUEUE","taskschd/TASK_INSTANCES_STOP_EXISTING"]
old-location: taskschd\task_instances_policy.htm
tech.root: taskschd
ms.assetid: 38d92951-546e-47e6-bc03-5ef4f317a814
ms.date: 12/05/2018
ms.keywords: TASK_INSTANCES_IGNORE_NEW, TASK_INSTANCES_PARALLEL, TASK_INSTANCES_POLICY, TASK_INSTANCES_POLICY enumeration [Task Scheduler], TASK_INSTANCES_QUEUE, TASK_INSTANCES_STOP_EXISTING, taskschd.task_instances_policy, taskschd/TASK_INSTANCES_IGNORE_NEW, taskschd/TASK_INSTANCES_PARALLEL, taskschd/TASK_INSTANCES_POLICY, taskschd/TASK_INSTANCES_QUEUE, taskschd/TASK_INSTANCES_STOP_EXISTING
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TASK_INSTANCES_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_INSTANCES_POLICY
 - taskschd/_TASK_INSTANCES_POLICY
 - TASK_INSTANCES_POLICY
 - taskschd/TASK_INSTANCES_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - taskschd.h
api_name:
 - TASK_INSTANCES_POLICY
---

# TASK_INSTANCES_POLICY enumeration


## -description

Defines how the Task Scheduler handles  existing instances of the task when it starts a new instance of the task.

## -enum-fields

### -field TASK_INSTANCES_PARALLEL:0

Starts new instance while an existing instance is running.

### -field TASK_INSTANCES_QUEUE:1

Starts a new instance of the task after all other instances of the task are complete.

### -field TASK_INSTANCES_IGNORE_NEW:2

Does not start a new instance if an existing instance of the task is running.

### -field TASK_INSTANCES_STOP_EXISTING:3

Stops an existing instance of the task before it starts a new instance.

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
