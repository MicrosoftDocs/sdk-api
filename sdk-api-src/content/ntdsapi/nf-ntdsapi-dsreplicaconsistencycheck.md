---
UID: NF:ntdsapi.DsReplicaConsistencyCheck
title: DsReplicaConsistencyCheck function (ntdsapi.h)
description: Invokes the Knowledge Consistency Checker (KCC) to verify the replication topology.
helpviewer_keywords: ["DS_KCC_FLAG_ASYNC_OP","DS_KCC_FLAG_DAMPED","DsReplicaConsistencyCheck","DsReplicaConsistencyCheck function [Active Directory]","_glines_dsreplicaconsistencycheck","ad.dsreplicaconsistencycheck","ntdsapi/DsReplicaConsistencyCheck"]
old-location: ad\dsreplicaconsistencycheck.htm
tech.root: ad
ms.assetid: 2a83ffcb-1ebd-4024-a186-9c079896f4e1
ms.date: 12/05/2018
ms.keywords: DS_KCC_FLAG_ASYNC_OP, DS_KCC_FLAG_DAMPED, DsReplicaConsistencyCheck, DsReplicaConsistencyCheck function [Active Directory], _glines_dsreplicaconsistencycheck, ad.dsreplicaconsistencycheck, ntdsapi/DsReplicaConsistencyCheck
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
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsReplicaConsistencyCheck
 - ntdsapi/DsReplicaConsistencyCheck
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsReplicaConsistencyCheck
---

# DsReplicaConsistencyCheck function


## -description

The <b>DsReplicaConsistencyCheck</b> function invokes the Knowledge Consistency Checker (KCC)  to verify the replication topology. The KCC dynamically adjusts the data replication topology of your network when domain controllers are added to or removed from the network, when a domain controller is unavailable, or when the data replication schedules are changed.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a>, 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a>, or <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithspna">DsBindWithSpn</a> function.

### -param TaskID [in]

Identifies the task that the KCC should execute. <b>DS_KCC_TASKID_UPDATE_TOPOLOGY</b> is the only currently supported value.

### -param dwFlags [in]

Contains a set of flags that modify the function behavior. This can be zero or a combination of one or more of the following values.



#### DS_KCC_FLAG_ASYNC_OP

The task is queued and then the function returns without waiting for the task to complete.



#### DS_KCC_FLAG_DAMPED

The task will not be added to the queue if another queued task will run soon.

## -returns

If the function performs its operation successfully, the return value is <b>ERROR_SUCCESS</b>. If the function fails, the return value can be one of the following.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_kcc_taskid">DS_KCC_TASKID</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithspna">DsBindWithSpn</a>