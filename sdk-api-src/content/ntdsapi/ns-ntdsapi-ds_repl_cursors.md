---
UID: NS:ntdsapi._DS_REPL_CURSORS
title: DS_REPL_CURSORS (ntdsapi.h)
description: The DS_REPL_CURSORS structure is used with the DsReplicaGetInfo and DsReplicaGetInfo2 function to provide replication state data with respect to all replicas of a given naming context.
helpviewer_keywords: ["DS_REPL_CURSORS","DS_REPL_CURSORS structure [Active Directory]","_glines_ds_repl_cursors","ad.ds__repl__cursors","ad.ds_repl_cursors","ntdsapi/DS_REPL_CURSORS"]
old-location: ad\ds_repl_cursors.htm
tech.root: ad
ms.assetid: 0fe5ad72-d3f3-42a8-a36f-ca1fc9c55c50
ms.date: 12/05/2018
ms.keywords: DS_REPL_CURSORS, DS_REPL_CURSORS structure [Active Directory], _glines_ds_repl_cursors, ad.ds__repl__cursors, ad.ds_repl_cursors, ntdsapi/DS_REPL_CURSORS
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
req.typenames: DS_REPL_CURSORS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_CURSORS
 - ntdsapi/_DS_REPL_CURSORS
 - DS_REPL_CURSORS
 - ntdsapi/DS_REPL_CURSORS
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
 - DS_REPL_CURSORS
---

# DS_REPL_CURSORS structure


## -description

The <b>DS_REPL_CURSORS</b> structure is used with the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> and <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function to provide replication state data with respect to all replicas of a given naming context.

## -struct-fields

### -field cNumCursors

Contains  the number of elements in the <b>rgCursor</b> array.

### -field dwReserved

Reserved for future use.

### -field rgCursor.size_is

### -field rgCursor.size_is.cNumCursors

### -field rgCursor

Contains an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursor">DS_REPL_CURSOR</a> structures that contain the requested replication data. The <b>cNumCursors</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursor">DS_REPL_CURSOR</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>