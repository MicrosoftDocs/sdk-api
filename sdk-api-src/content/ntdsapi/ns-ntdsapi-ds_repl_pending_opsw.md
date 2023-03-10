---
UID: NS:ntdsapi._DS_REPL_PENDING_OPSW
title: DS_REPL_PENDING_OPSW (ntdsapi.h)
description: Contains an array of DS_REPL_OP structures, which in turn describe the replication tasks currently executing and queued to execute, as returned by the DsReplicaGetInfo and DsReplicaGetInfo2 functions.
helpviewer_keywords: ["DS_REPL_PENDING_OPS","DS_REPL_PENDING_OPS structure [Active Directory]","DS_REPL_PENDING_OPSW","_DS_REPL_PENDING_OPSW","_glines_ds_repl_pending_ops","ad.ds__repl__pending__ops","ad.ds_repl_pending_ops","ntdsapi/DS_REPL_PENDING_OPS"]
old-location: ad\ds_repl_pending_ops.htm
tech.root: ad
ms.assetid: 2e4b96cb-fbd6-496b-aff3-cb7d82f1fa39
ms.date: 12/05/2018
ms.keywords: DS_REPL_PENDING_OPS, DS_REPL_PENDING_OPS structure [Active Directory], DS_REPL_PENDING_OPSW, _DS_REPL_PENDING_OPSW, _glines_ds_repl_pending_ops, ad.ds__repl__pending__ops, ad.ds_repl_pending_ops, ntdsapi/DS_REPL_PENDING_OPS
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
targetos: Windows
req.typenames: DS_REPL_PENDING_OPSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_PENDING_OPSW
 - ntdsapi/_DS_REPL_PENDING_OPSW
 - DS_REPL_PENDING_OPSW
 - ntdsapi/DS_REPL_PENDING_OPSW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_PENDING_OPS
---

# DS_REPL_PENDING_OPSW structure


## -description

The <b>DS_REPL_PENDING_OPS</b> structure contains an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_opw">DS_REPL_OP</a> structures, which in turn describe the replication tasks currently executing and queued to execute, as returned by the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> and <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> functions. The entries in the queue are processed in priority order, and the first entry is the one currently being executed.

## -struct-fields

### -field ftimeCurrentOpStarted

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time at which the first operation in the queue began executing.

### -field cNumPendingOps

Contains the number of elements in the <b>rgPendingOps</b> array.

### -field rgPendingOp.size_is

### -field rgPendingOp.size_is.cNumPendingOps

### -field rgPendingOp

Contains an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_opw">DS_REPL_OP</a> structures that contain the replication tasks currently executing and queued to execute.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_opw">DS_REPL_OP</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>