---
UID: NE:taskschd._TASK_RUNLEVEL
title: TASK_RUNLEVEL_TYPE (taskschd.h)
description: Defines LUA elevation flags that specify with what privilege level the task will be run.
helpviewer_keywords: ["TASK_RUNLEVEL_HIGHEST","TASK_RUNLEVEL_LUA","TASK_RUNLEVEL_TYPE","TASK_RUNLEVEL_TYPE enumeration [Task Scheduler]","taskschd.task_runlevel_type","taskschd/TASK_RUNLEVEL_HIGHEST","taskschd/TASK_RUNLEVEL_LUA","taskschd/TASK_RUNLEVEL_TYPE"]
old-location: taskschd\task_runlevel_type.htm
tech.root: taskschd
ms.assetid: 27e8e4c2-6898-4785-a311-b7fbbf7e0108
ms.date: 12/05/2018
ms.keywords: TASK_RUNLEVEL_HIGHEST, TASK_RUNLEVEL_LUA, TASK_RUNLEVEL_TYPE, TASK_RUNLEVEL_TYPE enumeration [Task Scheduler], taskschd.task_runlevel_type, taskschd/TASK_RUNLEVEL_HIGHEST, taskschd/TASK_RUNLEVEL_LUA, taskschd/TASK_RUNLEVEL_TYPE
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
req.typenames: TASK_RUNLEVEL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_RUNLEVEL
 - taskschd/_TASK_RUNLEVEL
 - TASK_RUNLEVEL_TYPE
 - taskschd/TASK_RUNLEVEL_TYPE
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
 - TASK_RUNLEVEL_TYPE
---

# TASK_RUNLEVEL_TYPE enumeration


## -description

Defines LUA elevation flags that specify with what privilege level the task will be run.

## -enum-fields

### -field TASK_RUNLEVEL_LUA:0

Tasks will be run with the least privileges.

### -field TASK_RUNLEVEL_HIGHEST:1

Tasks will be run with the highest privileges.

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
