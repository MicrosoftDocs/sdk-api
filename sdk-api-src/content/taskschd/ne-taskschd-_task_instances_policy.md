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

# _TASK_INSTANCES_POLICY enumeration


## -description


Defines how the Task Scheduler handles  existing instances of the task when it starts a new instance of the task.


## -enum-fields




### -field TASK_INSTANCES_PARALLEL

Starts new instance while an existing instance is running.


### -field TASK_INSTANCES_QUEUE

Starts a new instance of the task after all other instances of the task are complete.


### -field TASK_INSTANCES_IGNORE_NEW

Does not start a new instance if an existing instance of the task is running.


### -field TASK_INSTANCES_STOP_EXISTING

Stops an existing instance of the task before it starts a new instance.


## -see-also




<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

