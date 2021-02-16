---
UID: NS:ntdsapi._DS_REPL_NEIGHBORW_BLOB
title: DS_REPL_NEIGHBORW_BLOB (ntdsapi.h)
description: Contains inbound replication state data for a particular naming context and source server pair.
helpviewer_keywords: ["DS_REPL_NBR_COMPRESS_CHANGES","DS_REPL_NBR_DO_SCHEDULED_SYNCS","DS_REPL_NBR_FULL_SYNC_IN_PROGRESS","DS_REPL_NBR_FULL_SYNC_NEXT_PACKET","DS_REPL_NBR_NEVER_SYNCED","DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS","DS_REPL_NBR_SYNC_ON_STARTUP","DS_REPL_NBR_TWO_WAY_SYNC","DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT","DS_REPL_NBR_WRITEABLE","DS_REPL_NEIGHBORW_BLOB","DS_REPL_NEIGHBORW_BLOB structure [Active Directory]","ad.ds_repl_neighborw_blob","ntdsapi/DS_REPL_NEIGHBORW_BLOB"]
old-location: ad\ds_repl_neighborw_blob.htm
tech.root: ad
ms.assetid: 1a56968a-29ed-4c94-80ee-02bdd279f5c2
ms.date: 12/05/2018
ms.keywords: DS_REPL_NBR_COMPRESS_CHANGES, DS_REPL_NBR_DO_SCHEDULED_SYNCS, DS_REPL_NBR_FULL_SYNC_IN_PROGRESS, DS_REPL_NBR_FULL_SYNC_NEXT_PACKET, DS_REPL_NBR_NEVER_SYNCED, DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS, DS_REPL_NBR_SYNC_ON_STARTUP, DS_REPL_NBR_TWO_WAY_SYNC, DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT, DS_REPL_NBR_WRITEABLE, DS_REPL_NEIGHBORW_BLOB, DS_REPL_NEIGHBORW_BLOB structure [Active Directory], ad.ds_repl_neighborw_blob, ntdsapi/DS_REPL_NEIGHBORW_BLOB
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
req.typenames: DS_REPL_NEIGHBORW_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_NEIGHBORW_BLOB
 - ntdsapi/_DS_REPL_NEIGHBORW_BLOB
 - DS_REPL_NEIGHBORW_BLOB
 - ntdsapi/DS_REPL_NEIGHBORW_BLOB
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
 - DS_REPL_NEIGHBORW_BLOB
---

# DS_REPL_NEIGHBORW_BLOB structure


## -description

The <b>DS_REPL_NEIGHBORW_BLOB</b> structure contains  inbound replication state data for a particular naming context and source server pair. This structure is similar to the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_neighborw">DS_REPL_NEIGHBOR</a> structure, but is obtained from the <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-NCReplInboundNeighbors</b> attribute.

## -struct-fields

### -field oszNamingContext

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the naming context to which this replication state data pertains. Each naming context is replicated independently and has different associated neighbor data, even if the naming contexts are replicated from the same source server.

### -field oszSourceDsaDN

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the distinguished name of the directory service agent corresponding to the source server to which this replication state data pertains.  Each source server has different associated neighbor data.

### -field oszSourceDsaAddress

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the transport-specific network address of the source server. That is, a directory name service name for RPC/IP replication, or an SMTP address for an SMTP replication.

### -field oszAsyncIntersiteTransportDN

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the distinguished name of the <b>interSiteTransport</b> object that corresponds to the transport over which replication is performed. This member contains <b>NULL</b> for RPC/IP replication.

### -field dwReplicaFlags

Contains a set of flags that specify attributes and options for the replication data. This can be zero or a combination of one or more of the following flags.



#### DS_REPL_NBR_WRITEABLE

The local copy of the naming context is writable.



#### DS_REPL_NBR_SYNC_ON_STARTUP

Replication of this naming context from this source is attempted when the destination server is booted. This normally only applies to intra-site neighbors.



#### DS_REPL_NBR_DO_SCHEDULED_SYNCS

Perform replication on a schedule. This flag is normally set unless the schedule for this naming context/source is "never", that is, the empty schedule.



#### DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT

Perform replication indirectly through the Inter-Site Messaging Service. This flag is set only when replicating over SMTP. This flag is not set when replicating over inter-site RPC/IP.



#### DS_REPL_NBR_TWO_WAY_SYNC

If set, indicates that when inbound replication is complete, the destination server must tell the source server to synchronize in the reverse direction. This feature is used in dial-up scenarios where only one of the two servers can initiate a dial-up connection. For example, this option would be used in a corporate headquarters and branch office, where the branch office connects to the corporate headquarters over the Internet by means of a dial-up ISP connection.



#### DS_REPL_NBR_FULL_SYNC_IN_PROGRESS

The destination server is performing a full synchronization from the source server. Full synchronizations do not use vectors that create updates (<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursors">DS_REPL_CURSORS</a>) for filtering updates. Full synchronizations are not used as a part of the normal replication protocol.



#### DS_REPL_NBR_FULL_SYNC_NEXT_PACKET

The last packet from the source indicated a modification of an object that the destination server has not yet created. The next packet to be requested instructs the source server to put all attributes of the modified object into the packet.



#### DS_REPL_NBR_NEVER_SYNCED

A synchronization has never been successfully completed from this source.



#### DS_REPL_NBR_COMPRESS_CHANGES

Changes received from this source are to be compressed. This is normally set if, and only if, the source server is in a different site.



#### DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS

No change notifications should be received from this source. Normally set if, and only if, the source server is in a different site.

### -field dwReserved

Reserved for future use.

### -field uuidNamingContextObjGuid

Contains the <b>objectGuid</b> of the naming context that corresponds to <b>pszNamingContext</b>.

### -field uuidSourceDsaObjGuid

Contains the <b>objectGuid</b> of the <b>nTDSDSA</b> object that corresponds to <b>pszSourceDsaDN</b>.

### -field uuidSourceDsaInvocationID

Contains the invocation identifier used by the source server as of the last replication attempt.

### -field uuidAsyncIntersiteTransportObjGuid

Contains the <b>objectGuid</b> of the inter-site transport object that corresponds to <b>pszAsyncIntersiteTransportDN</b>.

### -field usnLastObjChangeSynced

Contains the update sequence number of the last object update received.

### -field usnAttributeFilter

Contains the <b>usnLastObjChangeSynced</b> value at the end of the last complete, successful replication cycle, or 0 if none. Attributes at the source last updated at a update sequence number less than or equal to this value have already been received and applied by the destination.

### -field ftimeLastSyncSuccess

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time the last successful replication cycle was completed from this source. All members of this structure are zero if the replication cycle has never been completed.

### -field ftimeLastSyncAttempt

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time of the last replication attempt from this source. All members of this structure are zero if the replication  has never been attempted.

### -field dwLastSyncResult

Contains a Windows error code associated with the last replication attempt from this source. Contains <b>ERROR_SUCCESS</b> if the last attempt was successful.

### -field cNumConsecutiveSyncFailures

Contains the number of failed replication attempts that have been made from this source since the last successful replication attempt or since the source was added as a neighbor, if no previous attempt succeeded.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_neighborw">DS_REPL_NEIGHBOR</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a>