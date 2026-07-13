---
UID: NF:ntdsapi.DsReplicaAddW
title: DsReplicaAddW function (ntdsapi.h)
description: Adds a replication source reference to a destination naming context. (Unicode)
helpviewer_keywords: ["DS_REPADD_ASYNCHRONOUS_OPERATION", "DS_REPADD_ASYNCHRONOUS_REPLICA", "DS_REPADD_DISABLE_NOTIFICATION", "DS_REPADD_DISABLE_PERIODIC", "DS_REPADD_INITIAL", "DS_REPADD_INTERSITE_MESSAGING", "DS_REPADD_NEVER_NOTIFY", "DS_REPADD_PERIODIC", "DS_REPADD_USE_COMPRESSION", "DS_REPADD_WRITEABLE", "DsReplicaAdd", "DsReplicaAdd function [Active Directory]", "DsReplicaAddW", "_glines_dsreplicaadd", "ad.dsreplicaadd", "ntdsapi/DsReplicaAdd", "ntdsapi/DsReplicaAddW"]
old-location: ad\dsreplicaadd.htm
tech.root: ad
ms.assetid: 33bd1b61-b9ed-479f-a128-fb7ddbb5e9af
ms.date: 12/05/2018
ms.keywords: DS_REPADD_ASYNCHRONOUS_OPERATION, DS_REPADD_ASYNCHRONOUS_REPLICA, DS_REPADD_DISABLE_NOTIFICATION, DS_REPADD_DISABLE_PERIODIC, DS_REPADD_INITIAL, DS_REPADD_INTERSITE_MESSAGING, DS_REPADD_NEVER_NOTIFY, DS_REPADD_PERIODIC, DS_REPADD_USE_COMPRESSION, DS_REPADD_WRITEABLE, DsReplicaAdd, DsReplicaAdd function [Active Directory], DsReplicaAddA, DsReplicaAddW, _glines_dsreplicaadd, ad.dsreplicaadd, ntdsapi/DsReplicaAdd, ntdsapi/DsReplicaAddA, ntdsapi/DsReplicaAddW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaAddW (Unicode) and DsReplicaAddA (ANSI)
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
 - DsReplicaAddW
 - ntdsapi/DsReplicaAddW
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
 - DsReplicaAdd
 - DsReplicaAddA
 - DsReplicaAddW
---

# DsReplicaAddW function


## -description

The <b>DsReplicaAdd</b> function adds a replication source reference to a destination naming context.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param NameContext [in]

The null-terminated string that specifies the distinguished name (DN) of the destination naming context (NC)  for which to add the replica. The destination NC record must exist locally as either an object, instantiated or not, or a reference phantom, for example, a phantom with a GUID.

### -param SourceDsaDn [in]

The null-terminated string that specifies the DN of the <b>NTDS-DSA</b> object for the source directory system agent. This parameter is required if <i>Options</i> includes <b>DS_REPADD_ASYNCHRONOUS_REPLICA</b>; otherwise, it is ignored.

### -param TransportDn [in]

The null-terminated string that specifies the DN of the <b>interSiteTransport</b> object that represents the transport used for communication with the source server. This parameter is required if <i>Options</i> includes <b>DS_REPADD_INTERSITE_MESSAGING</b>; otherwise, it is ignored.

### -param SourceDsaAddress [in]

The null-terminated string that specifies the transport-specific address of the source DSA. This source server is identified by a string name, not by its UUID. A string name appropriate for <i>SourceDsaAddress</i> is usually a DNS name based on a GUID, where the GUID part of the name is the GUID of the <b>NTDS-DSA</b> object for the source server.

### -param pSchedule [in]

Pointer to a <a href="/windows/desktop/api/schedule/ns-schedule-schedule">SCHEDULE</a> structure that contains the  replication schedule data for the replication source. This parameter is optional and can be <b>NULL</b> if not used.

### -param Options [in]

Passes additional data to be used to process the request. This parameter can be a combination of the following values.



#### DS_REPADD_ASYNCHRONOUS_OPERATION

Performs this operation asynchronously.



#### DS_REPADD_ASYNCHRONOUS_REPLICA

Does not replicate the NC. Instead, save enough state data such that it may be replicated later.



#### DS_REPADD_DISABLE_NOTIFICATION

Disables notification-based synchronization for the NC from this source. This is expected to be a temporary state. Use <b>DS_REPADD_NEVER_NOTIFY</b> to permanently disable synchronization.



#### DS_REPADD_DISABLE_PERIODIC

Disables periodic synchronization for the NC from this source.



#### DS_REPADD_INITIAL

Synchronizes the NC from this source when the DSA is started.



#### DS_REPADD_INTERSITE_MESSAGING

Synchronizes from the source DSA using the Intersite Messaging Service (IMS) transport, for example, by SMTP, rather than using the native directory service RPC.



#### DS_REPADD_NEVER_NOTIFY

Disables change notifications from this source. When this flag is set, the source does not notify the destination when changes occur. This is recommended for all intersite replication that may occur over WAN links.

This is expected to be a permanent state; use <b>DS_REPADD_DISABLE_NOTIFICATION</b> to temporarily disable notifications.



#### DS_REPADD_PERIODIC

Synchronizes the NC from this source periodically, as defined in <i>pSchedule</i>.



#### DS_REPADD_USE_COMPRESSION

Uses compression when replicating. This saves network bandwidth at the expense of CPU overhead at both the source and destination servers.



#### DS_REPADD_WRITEABLE

Creates a writable replica; otherwise, the replica is read-only.


##### - Options.DS_REPADD_ASYNCHRONOUS_OPERATION

Performs this operation asynchronously.


##### - Options.DS_REPADD_ASYNCHRONOUS_REPLICA

Does not replicate the NC. Instead, save enough state data such that it may be replicated later.


##### - Options.DS_REPADD_DISABLE_NOTIFICATION

Disables notification-based synchronization for the NC from this source. This is expected to be a temporary state. Use <b>DS_REPADD_NEVER_NOTIFY</b> to permanently disable synchronization.


##### - Options.DS_REPADD_DISABLE_PERIODIC

Disables periodic synchronization for the NC from this source.


##### - Options.DS_REPADD_INITIAL

Synchronizes the NC from this source when the DSA is started.


##### - Options.DS_REPADD_INTERSITE_MESSAGING

Synchronizes from the source DSA using the Intersite Messaging Service (IMS) transport, for example, by SMTP, rather than using the native directory service RPC.


##### - Options.DS_REPADD_NEVER_NOTIFY

Disables change notifications from this source. When this flag is set, the source does not notify the destination when changes occur. This is recommended for all intersite replication that may occur over WAN links.

This is expected to be a permanent state; use <b>DS_REPADD_DISABLE_NOTIFICATION</b> to temporarily disable notifications.


##### - Options.DS_REPADD_PERIODIC

Synchronizes the NC from this source periodically, as defined in <i>pSchedule</i>.


##### - Options.DS_REPADD_USE_COMPRESSION

Uses compression when replicating. This saves network bandwidth at the expense of CPU overhead at both the source and destination servers.


##### - Options.DS_REPADD_WRITEABLE

Creates a writable replica; otherwise, the replica is read-only.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value can be one of the following.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicadela">DsReplicaDel</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicamodifya">DsReplicaModify</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasynca">DsReplicaSync</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa">DsReplicaUpdateRefs</a>



<a href="/windows/desktop/api/schedule/ns-schedule-schedule">SCHEDULE</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsReplicaAdd as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
