---
UID: NE:taskschd._TASK_RUN_FLAGS
title: TASK_RUN_FLAGS (taskschd.h)
description: Defines how a task is run.
helpviewer_keywords: ["TASK_RUN_AS_SELF","TASK_RUN_FLAGS","TASK_RUN_FLAGS enumeration [Task Scheduler]","TASK_RUN_IGNORE_CONSTRAINTS","TASK_RUN_NO_FLAGS","TASK_RUN_USER_SID","TASK_RUN_USE_SESSION_ID","taskschd.task_run_flags","taskschd/TASK_RUN_AS_SELF","taskschd/TASK_RUN_FLAGS","taskschd/TASK_RUN_IGNORE_CONSTRAINTS","taskschd/TASK_RUN_NO_FLAGS","taskschd/TASK_RUN_USER_SID","taskschd/TASK_RUN_USE_SESSION_ID"]
old-location: taskschd\task_run_flags.htm
tech.root: taskschd
ms.assetid: 6c5a4ab6-b3ca-4d60-918d-82797782d66a
ms.date: 12/05/2018
ms.keywords: TASK_RUN_AS_SELF, TASK_RUN_FLAGS, TASK_RUN_FLAGS enumeration [Task Scheduler], TASK_RUN_IGNORE_CONSTRAINTS, TASK_RUN_NO_FLAGS, TASK_RUN_USER_SID, TASK_RUN_USE_SESSION_ID, taskschd.task_run_flags, taskschd/TASK_RUN_AS_SELF, taskschd/TASK_RUN_FLAGS, taskschd/TASK_RUN_IGNORE_CONSTRAINTS, taskschd/TASK_RUN_NO_FLAGS, taskschd/TASK_RUN_USER_SID, taskschd/TASK_RUN_USE_SESSION_ID
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
req.typenames: TASK_RUN_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_RUN_FLAGS
 - taskschd/_TASK_RUN_FLAGS
 - TASK_RUN_FLAGS
 - taskschd/TASK_RUN_FLAGS
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
 - TASK_RUN_FLAGS
---

# TASK_RUN_FLAGS enumeration


## -description

Defines how a task is run.

## -enum-fields

### -field TASK_RUN_NO_FLAGS:0

The task is run with all flags ignored.

### -field TASK_RUN_AS_SELF:0x1

The task is run as the user who is calling the <a href="/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run">Run</a> method.

### -field TASK_RUN_IGNORE_CONSTRAINTS:0x2

The task is run regardless of constraints such as "do not run on batteries" or "run only if idle".

### -field TASK_RUN_USE_SESSION_ID:0x4

The task is run using a terminal server session identifier.

### -field TASK_RUN_USER_SID:0x8

The task is run using a security identifier.

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
