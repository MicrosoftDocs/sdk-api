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

# _DS_REPL_PENDING_OPSW structure


## -description


The <b>DS_REPL_PENDING_OPS</b> structure contains an array of <a href="https://msdn.microsoft.com/9ea783b3-1529-4424-a582-f46f2a239a60">DS_REPL_OP</a> structures, which in turn describe the replication tasks currently executing and queued to execute, as returned by the 
<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions. The entries in the queue are processed in priority order, and the first entry is the one currently being executed.


## -struct-fields




### -field ftimeCurrentOpStarted

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time at which the first operation in the queue began executing.


### -field cNumPendingOps

Contains the number of elements in the <b>rgPendingOps</b> array.


### -field rgPendingOp.size_is

 


### -field rgPendingOp.size_is.cNumPendingOps

 


### -field rgPendingOp

Contains an array of <a href="https://msdn.microsoft.com/9ea783b3-1529-4424-a582-f46f2a239a60">DS_REPL_OP</a> structures that contain the replication tasks currently executing and queued to execute.


## -see-also




<a href="https://msdn.microsoft.com/9ea783b3-1529-4424-a582-f46f2a239a60">DS_REPL_OP</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

