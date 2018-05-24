---
UID: NS:ntdsapi._DS_REPL_PENDING_OPSW
title: "_DS_REPL_PENDING_OPSW"
author: windows-driver-content
description: Contains an array of DS_REPL_OP structures, which in turn describe the replication tasks currently executing and queued to execute, as returned by the DsReplicaGetInfo and DsReplicaGetInfo2 functions.
old-location: ad\ds_repl_pending_ops.htm
old-project: AD
ms.assetid: 2e4b96cb-fbd6-496b-aff3-cb7d82f1fa39
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: DS_REPL_PENDING_OPS, DS_REPL_PENDING_OPS structure [Active Directory], DS_REPL_PENDING_OPSW, _DS_REPL_PENDING_OPSW, _glines_ds_repl_pending_ops, ad.ds__repl__pending__ops, ad.ds_repl_pending_ops, ntdsapi/DS_REPL_PENDING_OPS
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DS_REPL_PENDING_OPSW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntdsapi.h
api_name:
-	DS_REPL_PENDING_OPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

