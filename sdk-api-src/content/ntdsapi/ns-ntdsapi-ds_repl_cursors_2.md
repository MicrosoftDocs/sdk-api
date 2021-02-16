---
UID: NS:ntdsapi._DS_REPL_CURSORS_2
title: DS_REPL_CURSORS_2 (ntdsapi.h)
description: The DS_REPL_CURSORS_2 structure is used with the DsReplicaGetInfo2 function to provide replication state data with respect to all replicas of a given naming context.
helpviewer_keywords: ["DS_REPL_CURSORS_2","DS_REPL_CURSORS_2 structure [Active Directory]","ad.ds_repl_cursors_2","ntdsapi/DS_REPL_CURSORS_2"]
old-location: ad\ds_repl_cursors_2.htm
tech.root: ad
ms.assetid: 5a1981ac-3b6a-4e48-8430-f8297ddd3283
ms.date: 12/05/2018
ms.keywords: DS_REPL_CURSORS_2, DS_REPL_CURSORS_2 structure [Active Directory], ad.ds_repl_cursors_2, ntdsapi/DS_REPL_CURSORS_2
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
req.typenames: DS_REPL_CURSORS_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_CURSORS_2
 - ntdsapi/_DS_REPL_CURSORS_2
 - DS_REPL_CURSORS_2
 - ntdsapi/DS_REPL_CURSORS_2
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
 - DS_REPL_CURSORS_2
---

# DS_REPL_CURSORS_2 structure


## -description

The <b>DS_REPL_CURSORS_2</b> structure is used with the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function to provide replication state data with respect to all replicas of a given naming context.

## -struct-fields

### -field cNumCursors

Contains  the number of elements in the <b>rgCursor</b> array.

### -field dwEnumerationContext

Contains the zero-based index of the next entry to retrieve if more entries are available. This value is passed for the <i>dwEnumerationContext</i> parameter in the next call to <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> to retrieve the next block of entries. If no more entries are available, this member contains -1.

### -field rgCursor.size_is

### -field rgCursor.size_is.cNumCursors

### -field rgCursor

Contains an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursor_2">DS_REPL_CURSOR_2</a> structures that contain the requested replication data. The <b>cNumCursors</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursor_2">DS_REPL_CURSOR_2</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>