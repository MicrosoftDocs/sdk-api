---
UID: NS:ntdsapi._DS_REPL_QUEUE_STATISTICSW
title: "_DS_REPL_QUEUE_STATISTICSW"
author: windows-sdk-content
description: Used to contain replication queue statistics.
old-location: ad\ds_repl_queue_statisticsw.htm
tech.root: ad
ms.assetid: bfddd7ed-0ff4-46ca-84c2-39020acb37d0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DS_REPL_QUEUE_STATISTICSW, DS_REPL_QUEUE_STATISTICSW structure [Active Directory], DS_REPL_QUEUE_STATISTICSW_BLOB, _DS_REPL_QUEUE_STATISTICSW, ad.ds_repl_queue_statisticsw, ntdsapi/DS_REPL_QUEUE_STATISTICSW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_QUEUE_STATISTICSW
product: Windows
targetos: Windows
req.typenames: DS_REPL_QUEUE_STATISTICSW, DS_REPL_QUEUE_STATISTICSW_BLOB
req.redist: 
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
 

 

