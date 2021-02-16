---
UID: NS:ntdsapi._DS_REPL_CURSOR
title: DS_REPL_CURSOR (ntdsapi.h)
description: The DS_REPL_CURSOR structure contains inbound replication state data with respect to all replicas of a given naming context, as returned by the DsReplicaGetInfo and DsReplicaGetInfo2 functions.
helpviewer_keywords: ["DS_REPL_CURSOR","DS_REPL_CURSOR structure [Active Directory]","_glines_ds_repl_cursor","ad.ds__repl__cursor","ad.ds_repl_cursor","ntdsapi/DS_REPL_CURSOR"]
old-location: ad\ds_repl_cursor.htm
tech.root: ad
ms.assetid: ab4ee8d8-5ccd-4f3f-a1c0-de78c65a10d3
ms.date: 12/05/2018
ms.keywords: DS_REPL_CURSOR, DS_REPL_CURSOR structure [Active Directory], _glines_ds_repl_cursor, ad.ds__repl__cursor, ad.ds_repl_cursor, ntdsapi/DS_REPL_CURSOR
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
req.typenames: DS_REPL_CURSOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_CURSOR
 - ntdsapi/_DS_REPL_CURSOR
 - DS_REPL_CURSOR
 - ntdsapi/DS_REPL_CURSOR
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
 - DS_REPL_CURSOR
---

# DS_REPL_CURSOR structure


## -description

The <b>DS_REPL_CURSOR</b> structure contains inbound replication state data with respect to all replicas of a given naming context, as returned by the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> and <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> functions.

## -struct-fields

### -field uuidSourceDsaInvocationID

Contains the invocation identifier of the originating server to which the <b>usnAttributeFilter</b> corresponds.

### -field usnAttributeFilter

Contains the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number. This is used to filter changes at replication source servers that the destination server has already applied.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursors">DS_REPL_CURSORS</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>