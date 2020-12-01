---
UID: NS:ntdsapi._DS_REPL_KCC_DSA_FAILUREW
title: DS_REPL_KCC_DSA_FAILUREW (ntdsapi.h)
description: The DS_REPL_KCC_DSA_FAILURE structure contains replication state data about a specific inbound replication partner, as returned by the DsReplicaGetInfo and DsReplicaGetInfo2 function.
helpviewer_keywords: ["DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES","DS_REPL_INFO_KCC_DSA_LINK_FAILURES","DS_REPL_KCC_DSA_FAILURE","DS_REPL_KCC_DSA_FAILURE structure [Active Directory]","DS_REPL_KCC_DSA_FAILUREW","DS_REPL_KCC_DSA_FAILUREW structure [Active Directory]","_glines_ds_repl_kcc_dsa_failure","ad.ds__repl__kcc__dsa__failure","ad.ds_repl_kcc_dsa_failure","ntdsapi/DS_REPL_KCC_DSA_FAILURE"]
old-location: ad\ds_repl_kcc_dsa_failure.htm
tech.root: ad
ms.assetid: 7a7131ce-a647-4b3d-a9f3-091b6dcebff7
ms.date: 12/05/2018
ms.keywords: DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES, DS_REPL_INFO_KCC_DSA_LINK_FAILURES, DS_REPL_KCC_DSA_FAILURE, DS_REPL_KCC_DSA_FAILURE structure [Active Directory], DS_REPL_KCC_DSA_FAILUREW, DS_REPL_KCC_DSA_FAILUREW structure [Active Directory], _glines_ds_repl_kcc_dsa_failure, ad.ds__repl__kcc__dsa__failure, ad.ds_repl_kcc_dsa_failure, ntdsapi/DS_REPL_KCC_DSA_FAILURE
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
req.typenames: DS_REPL_KCC_DSA_FAILUREW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_KCC_DSA_FAILUREW
 - ntdsapi/_DS_REPL_KCC_DSA_FAILUREW
 - DS_REPL_KCC_DSA_FAILUREW
 - ntdsapi/DS_REPL_KCC_DSA_FAILUREW
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
 - DS_REPL_KCC_DSA_FAILUREW
---

# DS_REPL_KCC_DSA_FAILUREW structure


## -description

The <b>DS_REPL_KCC_DSA_FAILURE</b> structure contains replication state data about a specific inbound replication partner, as returned by the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> and <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function. This state data is compiled and used by the Knowledge Consistency Checker (KCC) to decide when alternate replication routes must be added to account for unreachable servers.

## -struct-fields

### -field pszDsaDN

Pointer to a null-terminated string that contains the  distinguished name of the directory system agent object in the directory that corresponds to the source server.

### -field uuidDsaObjGuid

Contains the <b>objectGuid</b> of the directory system agent object represented by the <b>pszDsaDN</b> member.

### -field ftimeFirstFailure

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure which the contents of depends on the value passed for the <i>InfoType</i> parameter when <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> or <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function was called.



#### DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES

Contains the date and time that the first failure occurred when replicating from the source server.



#### DS_REPL_INFO_KCC_DSA_LINK_FAILURES

Contains the date and time of the last successful replication.

### -field cNumFailures

Contains the number of consecutive failures since the last successful replication.

### -field dwLastResult

Contains the error code associated with the most recent failure, or <b>ERROR_SUCCESS</b> if the specific error is unavailable.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw">DS_REPL_KCC_DSA_FAILURES</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>