---
UID: NF:ntdsapi.DsReplicaSyncAllA
title: DsReplicaSyncAllA function (ntdsapi.h)
description: Synchronizes a server with all other servers, using transitive replication, as necessary. (ANSI)
helpviewer_keywords: ["DS_REPSYNCALL_ABORT_IF_SERVER_UNAVAILABLE", "DS_REPSYNCALL_CROSS_SITE_BOUNDARIES", "DS_REPSYNCALL_DO_NOT_SYNC", "DS_REPSYNCALL_ID_SERVERS_BY_DN", "DS_REPSYNCALL_NO_OPTIONS", "DS_REPSYNCALL_PUSH_CHANGES_OUTWARD", "DS_REPSYNCALL_SKIP_INITIAL_CHECK", "DS_REPSYNCALL_SYNC_ADJACENT_SERVERS_ONLY", "DsReplicaSyncAllA", "ntdsapi/DsReplicaSyncAllA"]
old-location: ad\dsreplicasyncall.htm
tech.root: ad
ms.assetid: 2608adde-4f18-4048-a96f-d736ff09cd4b
ms.date: 12/05/2018
ms.keywords: DS_REPSYNCALL_ABORT_IF_SERVER_UNAVAILABLE, DS_REPSYNCALL_CROSS_SITE_BOUNDARIES, DS_REPSYNCALL_DO_NOT_SYNC, DS_REPSYNCALL_ID_SERVERS_BY_DN, DS_REPSYNCALL_NO_OPTIONS, DS_REPSYNCALL_PUSH_CHANGES_OUTWARD, DS_REPSYNCALL_SKIP_INITIAL_CHECK, DS_REPSYNCALL_SYNC_ADJACENT_SERVERS_ONLY, DsReplicaSyncAll, DsReplicaSyncAll function [Active Directory], DsReplicaSyncAllA, DsReplicaSyncAllW, ad.dsreplicasyncall, ntdsapi/DsReplicaSyncAll, ntdsapi/DsReplicaSyncAllA, ntdsapi/DsReplicaSyncAllW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaSyncAllW (Unicode) and DsReplicaSyncAllA (ANSI)
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
 - DsReplicaSyncAllA
 - ntdsapi/DsReplicaSyncAllA
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
 - DsReplicaSyncAll
 - DsReplicaSyncAllA
 - DsReplicaSyncAllW
---

# DsReplicaSyncAllA function


## -description

The <b>DsReplicaSyncAll</b> function synchronizes a server with all other servers, using transitive replication, as necessary. By default, <b>DsReplicaSyncAll</b> synchronizes the server with all other servers in its site; however, you can also use it to synchronize across site boundaries.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param pszNameContext [in]

Pointer to a null-terminated string that specifies the distinguished name of the naming context to synchronize. The <i>pszNameContext</i> parameter is optional; if its value is <b>NULL</b>, the configuration naming context is replicated.

### -param ulFlags [in]

Passes additional data used to process the request. This parameter can be a combination of the following values.



#### DS_REPSYNCALL_ABORT_IF_SERVER_UNAVAILABLE

Generates a fatal error if any server cannot be contacted or if any server is unreachable due to a disconnected or broken topology.



#### DS_REPSYNCALL_CROSS_SITE_BOUNDARIES

Synchronizes across site boundaries. By default, <b>DsReplicaSyncAll</b> attempts to synchronize only with DCs in the same site as the home system. Set this flag to attempt to synchronize with all DCs in the enterprise forest. However, the DCs can be synchronized only if connected by a synchronous (RPC) transport.



#### DS_REPSYNCALL_DO_NOT_SYNC

Disables all synchronization. The topology is still analyzed, and unavailable or unreachable servers are still identified.



#### DS_REPSYNCALL_ID_SERVERS_BY_DN

In the event of a non-fatal error, returns server distinguished names (DN) instead of their GUID DNS names.



#### DS_REPSYNCALL_NO_OPTIONS

This option has no effect.



#### DS_REPSYNCALL_PUSH_CHANGES_OUTWARD

Pushes changes from the home server out to all partners using transitive replication. This reverses the direction of replication, and the order of execution of the replication sets from the usual "pulling" mode of execution.



#### DS_REPSYNCALL_SKIP_INITIAL_CHECK

Assumes that all servers are responding. This speeds operation of the <b>DsReplicaSyncAll</b> function, but if some servers are not responding, some transitive replications may be blocked.



#### DS_REPSYNCALL_SYNC_ADJACENT_SERVERS_ONLY

Disables transitive replication. Synchronization is performed only with adjacent servers.

### -param pFnCallBack [in]

Pointer to an application-defined <a href="/previous-versions/windows/desktop/legacy/ms677968(v=vs.85)">SyncUpdateProc</a> function called by the <b>DsReplicaSyncAll</b> function when it encounters an error, initiates synchronization of two servers, completes synchronization of two servers, or finishes synchronization of all the servers in the site.



####

### -param pCallbackData [in, optional]

Pointer to application-defined data passed as the first argument of the <a href="/previous-versions/windows/desktop/legacy/ms677968(v=vs.85)">SyncUpdateProc</a> callback function pointed to by the <i>pFnCallBack</i> parameter.

### -param pErrors [out, optional]

A NULL-terminated array of pointers to  
<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa">DS_REPSYNCALL_ERRINFO</a> structures that contain errors that occurred during synchronization. The memory used to hold both the array of pointers and the MsCS\mscs\clusctl_resource_type_get_private_property_fmts.xml data is allocated as a single block of memory and should be freed when no longer required  by a single call to <b>LocalFree</b> with the pointer value returned in <i>pErrors</i> used as the argument.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is as follows.

## -remarks

The <b>DsReplicaSyncAll</b> function attempts to bind to all servers before generating a topology to synchronize from. If a server cannot be contacted, the function excludes that server from the topology and attempts to work around it. Setting the <b>DS_REPSYNCALL_SKIP_INITIAL_CHECK</b> flag in <i>ulFlags</i> bypasses the initial binding.

If a server cannot be contacted, the <b>DsReplicaSyncAll</b> function attempts to route around it and replicate from as many servers as possible, unless <b>DS_REPSYNCALL_ABORT_IF_SERVER_UNAVAILABLE</b> is set in <i>ulFlags</i>.

The <b>DsReplicaSyncAll</b> function can use the callback function pointed to by <i>pFnCallBack</i> to keep an end user informed about the current status of the replication. Execution of the <b>DsReplicaSyncAll</b> function pauses when it calls the function pointed to by <i>pFnCallBack</i>. If the return value from the callback function is <b>TRUE</b>, replication continues; otherwise, the <b>DsReplicaSyncAll</b> function terminates replication.





> [!NOTE]
> The ntdsapi.h header defines DsReplicaSyncAll as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa">DS_REPSYNCALL_ERRINFO</a>



<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_updatea">DS_REPSYNCALL_UPDATE</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication
  Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasynca">DsReplicaSync</a>



<a href="/previous-versions/windows/desktop/legacy/ms677968(v=vs.85)">SyncUpdateProc</a>
