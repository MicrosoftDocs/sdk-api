---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _TASK_RUN_FLAGS enumeration


## -description


Defines how a task is run.


## -enum-fields




### -field TASK_RUN_NO_FLAGS

The task is run with all flags ignored.


### -field TASK_RUN_AS_SELF

The task is run as the user who is calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a> method.


### -field TASK_RUN_IGNORE_CONSTRAINTS

The task is run regardless of constraints such as "do not run on batteries" or "run only if idle".


### -field TASK_RUN_USE_SESSION_ID

The task is run using a terminal server session identifier.


### -field TASK_RUN_USER_SID

The task is run using a security identifier.


## -see-also




<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

