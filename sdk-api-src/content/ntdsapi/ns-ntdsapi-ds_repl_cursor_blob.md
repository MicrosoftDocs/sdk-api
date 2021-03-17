---
UID: NS:ntdsapi._DS_REPL_CURSOR_BLOB
title: DS_REPL_CURSOR_BLOB (ntdsapi.h)
description: The DS_REPL_CURSOR_BLOB structure contains inbound replication state data with respect to all replicas of a given naming context.
helpviewer_keywords: ["DS_REPL_CURSOR_BLOB","DS_REPL_CURSOR_BLOB structure [Active Directory]","ad.ds_repl_cursor_blob","ntdsapi/DS_REPL_CURSOR_BLOB"]
old-location: ad\ds_repl_cursor_blob.htm
tech.root: ad
ms.assetid: c41e4737-5ef8-40ce-9af1-0afff7e11dc1
ms.date: 12/05/2018
ms.keywords: DS_REPL_CURSOR_BLOB, DS_REPL_CURSOR_BLOB structure [Active Directory], ad.ds_repl_cursor_blob, ntdsapi/DS_REPL_CURSOR_BLOB
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
req.typenames: DS_REPL_CURSOR_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_CURSOR_BLOB
 - ntdsapi/_DS_REPL_CURSOR_BLOB
 - DS_REPL_CURSOR_BLOB
 - ntdsapi/DS_REPL_CURSOR_BLOB
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
 - DS_REPL_CURSOR_BLOB
---

# DS_REPL_CURSOR_BLOB structure


## -description

The <b>DS_REPL_CURSOR_BLOB</b> structure contains inbound replication state data with respect to all replicas of a   given naming context. This structure is similar to the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursor_3w">DS_REPL_CURSOR_3</a> structure, but is obtained from the <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-NCReplCursors</b> attribute.

## -struct-fields

### -field uuidSourceDsaInvocationID

Contains the invocation identifier of the originating server to which the <b>usnAttributeFilter</b> corresponds.

### -field usnAttributeFilter

Contains the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number. This is used to filter changes at replication source servers that the destination server has already applied.

### -field ftimeLastSyncSuccess

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time of the last successful synchronization operation.

### -field oszSourceDsaDN

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the distinguished name of the directory service agent that corresponds to the source server to which this replication state data applies.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursor_3w">DS_REPL_CURSOR_3</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a>