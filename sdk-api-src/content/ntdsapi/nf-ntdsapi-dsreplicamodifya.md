---
UID: NF:ntdsapi.DsReplicaModifyA
title: DsReplicaModifyA function (ntdsapi.h)
description: Modifies an existing replication source reference for a destination naming context. (ANSI)
helpviewer_keywords: ["DS_REPL_NBR_COMPRESS_CHANGES", "DS_REPL_NBR_DISABLE_SCHEDULED_SYNC", "DS_REPL_NBR_DO_SCHEDULED_SYNCS", "DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS", "DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS", "DS_REPL_NBR_SYNC_ON_STARTUP", "DS_REPL_NBR_TWO_WAY_SYNC", "DS_REPMOD_ASYNCHRONOUS_OPERATION", "DS_REPMOD_UPDATE_ADDRESS", "DS_REPMOD_UPDATE_FLAGS", "DS_REPMOD_UPDATE_RESULT", "DS_REPMOD_UPDATE_SCHEDULE", "DS_REPMOD_UPDATE_TRANSPORT", "DS_REPMOD_WRITEABLE", "DsReplicaModifyA", "ntdsapi/DsReplicaModifyA"]
old-location: ad\dsreplicamodify.htm
tech.root: ad
ms.assetid: aad20527-1211-41bc-b0e9-02e4ab28ae2e
ms.date: 12/05/2018
ms.keywords: DS_REPL_NBR_COMPRESS_CHANGES, DS_REPL_NBR_DISABLE_SCHEDULED_SYNC, DS_REPL_NBR_DO_SCHEDULED_SYNCS, DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS, DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS, DS_REPL_NBR_SYNC_ON_STARTUP, DS_REPL_NBR_TWO_WAY_SYNC, DS_REPMOD_ASYNCHRONOUS_OPERATION, DS_REPMOD_UPDATE_ADDRESS, DS_REPMOD_UPDATE_FLAGS, DS_REPMOD_UPDATE_RESULT, DS_REPMOD_UPDATE_SCHEDULE, DS_REPMOD_UPDATE_TRANSPORT, DS_REPMOD_WRITEABLE, DsReplicaModify, DsReplicaModify function [Active Directory], DsReplicaModifyA, DsReplicaModifyW, _glines_dsreplicamodify, ad.dsreplicamodify, ntdsapi/DsReplicaModify, ntdsapi/DsReplicaModifyA, ntdsapi/DsReplicaModifyW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaModifyW (Unicode) and DsReplicaModifyA (ANSI)
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
 - DsReplicaModifyA
 - ntdsapi/DsReplicaModifyA
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
 - DsReplicaModify
 - DsReplicaModifyA
 - DsReplicaModifyW
---

# DsReplicaModifyA function


## -description

The <b>DsReplicaModify</b> function modifies an existing replication source reference for a destination naming context.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param NameContext [in]

Pointer to a constant null-terminated string that specifies the distinguished name (DN) of the destination naming context (NC).

### -param pUuidSourceDsa [in]

Pointer to the UUID of the source directory system agent (DSA). This parameter may be null if <i>ModifyFields</i> does not include <b>DS_REPMOD_UPDATE_ADDRESS</b> and <i>SourceDsaAddress</i> is not <b>NULL</b>.

### -param TransportDn [in]

Reserved for future use. Any value other than <b>NULL</b> results in <b>ERROR_NOT_SUPPORTED</b> being returned.

### -param SourceDsaAddress [in]

Pointer to a constant null-terminated Unicode string that specifies the transport-specific address of the source DSA. This parameter is ignored if <i>pUuidSourceDsa</i> is not <b>NULL</b> and <i>ModifyFields</i> does not include <b>DS_REPMOD_UPDATE_ADDRESS</b>.

### -param pSchedule [in]

Pointer to a <a href="/windows/desktop/api/schedule/ns-schedule-schedule">SCHEDULE</a> structure that contains the  replication schedule data for the replication source. This parameter is optional and can be <b>NULL</b> if not used. This parameter is required if <i>ModifyFields</i> contains the  <b>DS_REPMOD_UPDATE_SCHEDULE</b> flag.

### -param ReplicaFlags [in]

This parameter is used to control replication behavior and can take the following values.



#### DS_REPL_NBR_SYNC_ON_STARTUP

Replication of this naming context from this source is attempted when the destination server is booted. This normally only applies to intra-site neighbors.



#### DS_REPL_NBR_DO_SCHEDULED_SYNCS

Perform replication on a schedule. This flag is normally set unless the schedule for this naming context and source is "never", that is, the empty schedule.



#### DS_REPL_NBR_TWO_WAY_SYNC

If set, indicates that when inbound replication is complete, the destination server must tell the source server to synchronize in the reverse direction. This feature is used in dial-up scenarios where only one of the two servers can initiate a dial-up connection. For example, this option would be used in a corporate headquarters and branch office, where the branch office connects to the corporate headquarters over the Internet by means of a dial-up ISP connection.



#### DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS

This neighbor is set to disable notification-based synchronization. Within a site, domain controllers synchronize with each other based on notifications when changes occur. This setting prevents this neighbor from performing a synchronization triggered by a notification. The neighbor will still do synchronization based on its schedule or in response to manually requested synchronization.



#### DS_REPL_NBR_DISABLE_SCHEDULED_SYNC

This neighbor is set to not perform synchronization based on its schedule. The only way this neighbor will perform synchronization is in response to change notifications or to manually requested synchronization.



#### DS_REPL_NBR_COMPRESS_CHANGES

Changes received from this source are to be compressed. This is normally set if, and only if, the source server is in a different site.



#### DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS

No change notifications should be received from this source. This is normally set if, and only if, the source server is in a different site.

### -param ModifyFields [in]

Specifies what fields should be modified. At least one field must be specified in <i>ModifyFields</i>. This parameter can be a combination of the following values.



#### DS_REPMOD_UPDATE_ADDRESS

Updates the address associated with the referenced server.



#### DS_REPMOD_UPDATE_FLAGS

Updates the flags associated with the replica.



#### DS_REPMOD_UPDATE_RESULT

Not used. Specifying updates of result values is not currently supported. Result values default to 0.



#### DS_REPMOD_UPDATE_SCHEDULE

Updates the periodic replication schedule associated with the replica.



#### DS_REPMOD_UPDATE_TRANSPORT

Updates the transport associated with the replica.

### -param Options [in]

Passes additional data used to process the request. This parameter can be a combination of the following values.



#### DS_REPMOD_ASYNCHRONOUS_OPERATION

Performs this operation asynchronously.



#### DS_REPMOD_WRITEABLE

Indicates that the replica being modified can be written to.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value can be one of the following.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaadda">DsReplicaAdd</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicadela">DsReplicaDel</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasynca">DsReplicaSync</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa">DsReplicaUpdateRefs</a>



<a href="/windows/desktop/api/schedule/ns-schedule-schedule">SCHEDULE</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsReplicaModify as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
