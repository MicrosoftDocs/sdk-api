---
UID: NE:taskschd._TASK_STATE
title: TASK_STATE (taskschd.h)
description: Defines the different states that a registered task can be in.
helpviewer_keywords: ["TASK_STATE","TASK_STATE enumeration [Task Scheduler]","TASK_STATE_DISABLED","TASK_STATE_QUEUED","TASK_STATE_READY","TASK_STATE_RUNNING","TASK_STATE_UNKNOWN","taskschd.task_state","taskschd/TASK_STATE","taskschd/TASK_STATE_DISABLED","taskschd/TASK_STATE_QUEUED","taskschd/TASK_STATE_READY","taskschd/TASK_STATE_RUNNING","taskschd/TASK_STATE_UNKNOWN"]
old-location: taskschd\task_state.htm
tech.root: taskschd
ms.assetid: 89fd8b0b-1cdf-4222-99cc-d8c55a3e68d6
ms.date: 12/05/2018
ms.keywords: TASK_STATE, TASK_STATE enumeration [Task Scheduler], TASK_STATE_DISABLED, TASK_STATE_QUEUED, TASK_STATE_READY, TASK_STATE_RUNNING, TASK_STATE_UNKNOWN, taskschd.task_state, taskschd/TASK_STATE, taskschd/TASK_STATE_DISABLED, taskschd/TASK_STATE_QUEUED, taskschd/TASK_STATE_READY, taskschd/TASK_STATE_RUNNING, taskschd/TASK_STATE_UNKNOWN
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
req.typenames: TASK_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_STATE
 - taskschd/_TASK_STATE
 - TASK_STATE
 - taskschd/TASK_STATE
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
 - TASK_STATE
---

# TASK_STATE enumeration


## -description

Defines the different states that a registered task can be in.

## -enum-fields

### -field TASK_STATE_UNKNOWN:0

The state of the task is unknown.

### -field TASK_STATE_DISABLED:1

The task is registered but is disabled and no instances of the task are queued or running. The task cannot be run until it is enabled.

### -field TASK_STATE_QUEUED:2

Instances of the task are queued.

### -field TASK_STATE_READY:3

The task is ready to be executed, but no instances are queued or running.

### -field TASK_STATE_RUNNING:4

One or more instances of the task is running.

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
