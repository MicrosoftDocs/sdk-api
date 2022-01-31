---
UID: NE:taskschd._TASK_COMPATIBILITY
title: TASK_COMPATIBILITY (taskschd.h)
description: Defines what versions of Task Scheduler or the AT command that the task is compatible with.
helpviewer_keywords: ["TASK_COMPATIBILITY","TASK_COMPATIBILITY enumeration [Task Scheduler]","TASK_COMPATIBILITY_AT","TASK_COMPATIBILITY_V1","TASK_COMPATIBILITY_V2","taskschd.task_compatibility","taskschd/TASK_COMPATIBILITY","taskschd/TASK_COMPATIBILITY_AT","taskschd/TASK_COMPATIBILITY_V1","taskschd/TASK_COMPATIBILITY_V2"]
old-location: taskschd\task_compatibility.htm
tech.root: taskschd
ms.assetid: a842ab84-26e1-49bd-bf57-1a1073a17183
ms.date: 12/05/2018
ms.keywords: TASK_COMPATIBILITY, TASK_COMPATIBILITY enumeration [Task Scheduler], TASK_COMPATIBILITY_AT, TASK_COMPATIBILITY_V1, TASK_COMPATIBILITY_V2, taskschd.task_compatibility, taskschd/TASK_COMPATIBILITY, taskschd/TASK_COMPATIBILITY_AT, taskschd/TASK_COMPATIBILITY_V1, taskschd/TASK_COMPATIBILITY_V2
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
req.typenames: TASK_COMPATIBILITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASK_COMPATIBILITY
 - taskschd/_TASK_COMPATIBILITY
 - TASK_COMPATIBILITY
 - taskschd/TASK_COMPATIBILITY
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
 - TASK_COMPATIBILITY
---

# TASK_COMPATIBILITY enumeration


## -description

 Defines what versions of Task Scheduler or the AT command that the task is compatible with.

## -enum-fields

### -field TASK_COMPATIBILITY_AT:0

The task is compatible with the AT command.

### -field TASK_COMPATIBILITY_V1:1

The task is compatible with Task Scheduler 1.0.

### -field TASK_COMPATIBILITY_V2:2

The task is compatible with Task Scheduler 2.0.

### -field TASK_COMPATIBILITY_V2_1:3

### -field TASK_COMPATIBILITY_V2_2:4

### -field TASK_COMPATIBILITY_V2_3:5

### -field TASK_COMPATIBILITY_V2_4:6

## -remarks

 Task compatibility, which is set through the <a href="/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility">Compatibility</a> property, should only be set to TASK_COMPATIBILITY_V1 if a task needs to be accessed or modified from a  Windows XP, Windows Server 2003, or Windows 2000 computer. Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.

Once the task <a href="/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility">Compatibility</a> property is set to TASK_COMPATIBILITY_V2 and the task is registered, then the task <b>Compatibility</b> property cannot be changed to TASK_COMPATIBILITY_V1.

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-enumerated-types">Task Scheduler Enumerated Types</a>
