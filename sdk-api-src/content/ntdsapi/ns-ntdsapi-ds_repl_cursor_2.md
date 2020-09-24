---
UID: NS:ntdsapi._DS_REPL_CURSOR_2
title: DS_REPL_CURSOR_2 (ntdsapi.h)
description: The DS_REPL_CURSOR_2 structure contains inbound replication state data with respect to all replicas of a given naming context, as returned by the DsReplicaGetInfo2 function. This structure is an enhanced version of the DS_REPL_CURSOR structure.
helpviewer_keywords: ["DS_REPL_CURSOR_2","DS_REPL_CURSOR_2 structure [Active Directory]","ad.ds_repl_cursor_2","ntdsapi/DS_REPL_CURSOR_2"]
old-location: ad\ds_repl_cursor_2.htm
tech.root: ad
ms.assetid: ff839372-41f0-499a-9582-59ace02f1485
ms.date: 12/05/2018
ms.keywords: DS_REPL_CURSOR_2, DS_REPL_CURSOR_2 structure [Active Directory], ad.ds_repl_cursor_2, ntdsapi/DS_REPL_CURSOR_2
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
req.typenames: DS_REPL_CURSOR_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_CURSOR_2
 - ntdsapi/_DS_REPL_CURSOR_2
 - DS_REPL_CURSOR_2
 - ntdsapi/DS_REPL_CURSOR_2
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
 - DS_REPL_CURSOR_2
---

# DS_REPL_CURSOR_2 structure


## -description

The <b>DS_REPL_CURSOR_2</b> structure contains inbound replication state data with respect to all replicas of a given naming context, as returned by the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function. This structure is an enhanced version of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursor">DS_REPL_CURSOR</a> structure.

## -struct-fields

### -field uuidSourceDsaInvocationID

Contains the invocation identifier of the originating server to which the <b>usnAttributeFilter</b> corresponds.

### -field usnAttributeFilter

Contains the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number. This is used to filter changes at replication source servers that the destination server has already applied.

### -field ftimeLastSyncSuccess

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time of the last successful synchronization operation.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursor">DS_REPL_CURSOR</a>



<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursors_2">DS_REPL_CURSORS_2</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>