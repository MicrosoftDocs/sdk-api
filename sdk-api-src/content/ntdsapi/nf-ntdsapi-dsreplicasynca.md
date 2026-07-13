---
UID: NF:ntdsapi.DsReplicaSyncA
title: DsReplicaSyncA function (ntdsapi.h)
description: Synchronizes a destination naming context (NC) with one of its sources. (ANSI)
helpviewer_keywords: ["DS_REPSYNC_ADD_REFERENCE", "DS_REPSYNC_ALL_SOURCES", "DS_REPSYNC_ASYNCHRONOUS_OPERATION", "DS_REPSYNC_FORCE", "DS_REPSYNC_FULL", "DS_REPSYNC_INTERSITE_MESSAGING", "DS_REPSYNC_NO_DISCARD", "DS_REPSYNC_PERIODIC", "DS_REPSYNC_URGENT", "DS_REPSYNC_WRITEABLE", "DsReplicaSyncA", "ntdsapi/DsReplicaSyncA"]
old-location: ad\dsreplicasync.htm
tech.root: ad
ms.assetid: 20c7f96d-f298-4321-a6f5-910c25e418db
ms.date: 12/05/2018
ms.keywords: DS_REPSYNC_ADD_REFERENCE, DS_REPSYNC_ALL_SOURCES, DS_REPSYNC_ASYNCHRONOUS_OPERATION, DS_REPSYNC_FORCE, DS_REPSYNC_FULL, DS_REPSYNC_INTERSITE_MESSAGING, DS_REPSYNC_NO_DISCARD, DS_REPSYNC_PERIODIC, DS_REPSYNC_URGENT, DS_REPSYNC_WRITEABLE, DsReplicaSync, DsReplicaSync function [Active Directory], DsReplicaSyncA, DsReplicaSyncW, _glines_dsreplicasync, ad.dsreplicasync, ntdsapi/DsReplicaSync, ntdsapi/DsReplicaSyncA, ntdsapi/DsReplicaSyncW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaSyncW (Unicode) and DsReplicaSyncA (ANSI)
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
 - DsReplicaSyncA
 - ntdsapi/DsReplicaSyncA
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
 - DsReplicaSync
 - DsReplicaSyncA
 - DsReplicaSyncW
---

# DsReplicaSyncA function


## -description

The <b>DsReplicaSync</b> function synchronizes a destination naming context (NC) with one of its sources.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param NameContext [in]

Pointer to a constant null-terminated string that specifies the distinguished name of the destination NC.

### -param pUuidDsaSrc [in]

Pointer to the UUID of a source that replicates to the destination NC.

### -param Options [in]

Passes additional data used to process the request. This parameter can be a combination of the following values.



#### DS_REPSYNC_ADD_REFERENCE

Causes the source directory system agent (DSA) to verify that the local DSA is present in the source replicates-to list. If not, the local DSA is added. This ensures that the source sends change notifications.



#### DS_REPSYNC_ALL_SOURCES

This value is not supported.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Synchronizes from all sources.



#### DS_REPSYNC_ASYNCHRONOUS_OPERATION

Performs this operation asynchronously.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Required when using <b>DS_REPSYNC_ALL_SOURCES</b>.



#### DS_REPSYNC_FORCE

Synchronizes even if the link is currently disabled.



#### DS_REPSYNC_FULL

Synchronizes starting from the first Update Sequence Number (USN).



#### DS_REPSYNC_INTERSITE_MESSAGING

Synchronizes using an ISM.



#### DS_REPSYNC_NO_DISCARD

Does not discard this synchronization request, even if a similar synchronization is pending.



#### DS_REPSYNC_PERIODIC

Indicates this operation is a periodic synchronization request as scheduled by the administrator.



#### DS_REPSYNC_URGENT

Indicates this operation is a notification of an update marked urgent.



#### DS_REPSYNC_WRITEABLE

Replica is writable. Otherwise, it is read-only.

## -returns

If the function performs its operation successfully, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the standard Win32 API errors.

## -remarks

The server that <b>DsReplicaSync</b> executes on is called the destination. The destination naming context is brought up-to-date with respect to a source system, identified by the UUID of the source system NTDS Settings object. The destination system must already be configured so that the source system is one of the systems from which it receives replication data.

<div class="alert"><b>Note</b>  Forcing manual synchronization can prevent the directory service from properly prioritizing replication operations. For example, synchronizing a new user may preempt an urgent synchronization performed to provide access to a recently locked out user or to add a new trust password. If you call this API often, you can flood the network with requests, which can interfere with other replication operations. For this reason, it is strongly recommended that this function be used only for single-use scenarios rather than incorporating it into an application that would use it on a regular basis.</div>
<div> </div>




> [!NOTE]
> The ntdsapi.h header defines DsReplicaSync as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaadda">DsReplicaAdd</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicadela">DsReplicaDel</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicamodifya">DsReplicaModify</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa">DsReplicaUpdateRefs</a>
