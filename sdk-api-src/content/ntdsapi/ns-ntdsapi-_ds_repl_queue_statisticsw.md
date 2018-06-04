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

# _DS_REPL_QUEUE_STATISTICSW structure


## -description


The <b>DS_REPL_QUEUE_STATISTICSW</b> structure is used to contain replication queue statistics.

Reserved. Obtain this data using the <a href="https://msdn.microsoft.com/13fe2237-d20c-4314-ab9a-5bf790742da0">DS_REPL_QUEUE_STATISTICSW_BLOB</a> structure with the <a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a> functions to obtain binary data for the <b>msDS-ReplQueueStatistics</b> attribute.


## -struct-fields




### -field ftimeCurrentOpStarted

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time that the currently running operation started.


### -field cNumPendingOps

Contains the number of currently pending operations.


### -field ftimeOldestSync

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time of the oldest synchronization operation.


### -field ftimeOldestAdd

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time of the oldest add operation.


### -field ftimeOldestMod

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time of the oldest modification operation.


### -field ftimeOldestDel

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time of the oldest delete operation.


### -field ftimeOldestUpdRefs

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time of the oldest reference update operation.


## -remarks




<a href="https://msdn.microsoft.com/13fe2237-d20c-4314-ab9a-5bf790742da0">DS_REPL_QUEUE_STATISTICSW_BLOB</a> is an alias for this structure.




## -see-also




<a href="https://msdn.microsoft.com/13fe2237-d20c-4314-ab9a-5bf790742da0">DS_REPL_QUEUE_STATISTICSW_BLOB</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>
 

 

