---
UID: NS:ntdsapi._DS_REPL_KCC_DSA_FAILUREW
title: "_DS_REPL_KCC_DSA_FAILUREW"
author: windows-sdk-content
description: The DS_REPL_KCC_DSA_FAILURE structure contains replication state data about a specific inbound replication partner, as returned by the DsReplicaGetInfo and DsReplicaGetInfo2 function.
old-location: ad\ds_repl_kcc_dsa_failure.htm
tech.root: ad
ms.assetid: 7a7131ce-a647-4b3d-a9f3-091b6dcebff7
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES, DS_REPL_INFO_KCC_DSA_LINK_FAILURES, DS_REPL_KCC_DSA_FAILURE, DS_REPL_KCC_DSA_FAILURE structure [Active Directory], DS_REPL_KCC_DSA_FAILUREW, DS_REPL_KCC_DSA_FAILUREW structure [Active Directory], _DS_REPL_KCC_DSA_FAILUREW, _glines_ds_repl_kcc_dsa_failure, ad.ds__repl__kcc__dsa__failure, ad.ds_repl_kcc_dsa_failure, ntdsapi/DS_REPL_KCC_DSA_FAILURE
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
 - DS_REPL_KCC_DSA_FAILUREW
product: Windows
targetos: Windows
req.typenames: DS_REPL_KCC_DSA_FAILUREW
req.redist: 
---

# _DS_REPL_KCC_DSA_FAILUREW structure


## -description


The <b>DS_REPL_KCC_DSA_FAILURE</b> structure contains replication state data about a specific inbound replication partner, as returned by the 
<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function. This state data is compiled and used by the Knowledge Consistency Checker (KCC) to decide when alternate replication routes must be added to account for unreachable servers.


## -struct-fields




### -field pszDsaDN

Pointer to a null-terminated string that contains the  distinguished name of the directory system agent object in the directory that corresponds to the source server.


### -field uuidDsaObjGuid

Contains the <b>objectGuid</b> of the directory system agent object represented by the <b>pszDsaDN</b> member.


### -field ftimeFirstFailure

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure which the contents of depends on the value passed for the <i>InfoType</i> parameter when <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> or <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function was called.



#### DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES

Contains the date and time that the first failure occurred when replicating from the source server.



#### DS_REPL_INFO_KCC_DSA_LINK_FAILURES

Contains the date and time of the last successful replication.


### -field cNumFailures

Contains the number of consecutive failures since the last successful replication.


### -field dwLastResult

Contains the error code associated with the most recent failure, or <b>ERROR_SUCCESS</b> if the specific error is unavailable.


## -see-also




<a href="https://msdn.microsoft.com/bb011502-38ae-43b7-a6ad-de16b499f61b">DS_REPL_KCC_DSA_FAILURES</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>
 

 

