---
UID: NE:taskschd._TASK_RUN_FLAGS
title: "_TASK_RUN_FLAGS"
author: windows-sdk-content
description: Defines how a task is run.
old-location: taskschd\task_run_flags.htm
old-project: taskschd
ms.assetid: 6c5a4ab6-b3ca-4d60-918d-82797782d66a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TASK_RUN_AS_SELF, TASK_RUN_FLAGS, TASK_RUN_FLAGS enumeration [Task Scheduler], TASK_RUN_IGNORE_CONSTRAINTS, TASK_RUN_NO_FLAGS, TASK_RUN_USER_SID, TASK_RUN_USE_SESSION_ID, _TASK_RUN_FLAGS, taskschd.task_run_flags, taskschd/TASK_RUN_AS_SELF, taskschd/TASK_RUN_FLAGS, taskschd/TASK_RUN_IGNORE_CONSTRAINTS, taskschd/TASK_RUN_NO_FLAGS, taskschd/TASK_RUN_USER_SID, taskschd/TASK_RUN_USE_SESSION_ID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: taskschd.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TASK_RUN_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - taskschd.h
api_name:
 - TASK_RUN_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _TASK_RUN_FLAGS enumeration


## -description


Defines how a task is run.


## -enum-fields




### -field TASK_RUN_NO_FLAGS

The task is run with all flags ignored.


### -field TASK_RUN_AS_SELF

The task is run as the user who is calling the <a href="https://msdn.microsoft.com/6b237ddd-e4e8-47f7-97e7-360e79841acc">Run</a> method.


### -field TASK_RUN_IGNORE_CONSTRAINTS

The task is run regardless of constraints such as "do not run on batteries" or "run only if idle".


### -field TASK_RUN_USE_SESSION_ID

The task is run using a terminal server session identifier.


### -field TASK_RUN_USER_SID

The task is run using a security identifier.


## -see-also




<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

