---
UID: NS:ntdsapi._DS_REPL_OPW_BLOB
title: DS_REPL_OPW_BLOB (ntdsapi.h)
description: The DS_REPL_OPW_BLOB structure describes a replication task currently executing or pending execution.
helpviewer_keywords: ["DS_REPL_OPW_BLOB","DS_REPL_OPW_BLOB structure [Active Directory]","DS_REPL_OP_TYPE_ADD","DS_REPL_OP_TYPE_DELETE","DS_REPL_OP_TYPE_MODIFY","DS_REPL_OP_TYPE_SYNC","DS_REPL_OP_TYPE_UPDATE_REFS","ad.ds_repl_opw_blob","ntdsapi/DS_REPL_OPW_BLOB"]
old-location: ad\ds_repl_opw_blob.htm
tech.root: ad
ms.assetid: 14676159-cc31-4254-b174-dcd84d9ceec1
ms.date: 12/05/2018
ms.keywords: DS_REPL_OPW_BLOB, DS_REPL_OPW_BLOB structure [Active Directory], DS_REPL_OP_TYPE_ADD, DS_REPL_OP_TYPE_DELETE, DS_REPL_OP_TYPE_MODIFY, DS_REPL_OP_TYPE_SYNC, DS_REPL_OP_TYPE_UPDATE_REFS, ad.ds_repl_opw_blob, ntdsapi/DS_REPL_OPW_BLOB
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
req.typenames: DS_REPL_OPW_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_OPW_BLOB
 - ntdsapi/_DS_REPL_OPW_BLOB
 - DS_REPL_OPW_BLOB
 - ntdsapi/DS_REPL_OPW_BLOB
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
 - DS_REPL_OPW_BLOB
---

# DS_REPL_OPW_BLOB structure


## -description

The <b>DS_REPL_OPW_BLOB</b> structure describes a replication task currently executing or pending execution. This structure is similar to the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_opw">DS_REPL_OP</a> structure, but is obtained from the <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-ReplPendingOps</b> attribute.

## -struct-fields

### -field ftimeEnqueued

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time that this operation was added to the queue.

### -field ulSerialNumber

Contains the identifier of the operation. This value is unique  in the startup routine of every computer. When the computer is restarted, the identifiers are no longer unique.

### -field ulPriority

Contains the priority value of this operation. Tasks with a higher priority value are executed first. The priority is calculated by the server based on the type of operation and its parameters.

### -field OpType

Contains one of the <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repl_op_type">DS_REPL_OP_TYPE</a> values that indicate the type of operation that this structure represents.

### -field ulOptions

Zero or more bits, the interpretation of which depends on the <b>OpType</b>. For <b>DS_REPL_OP_TYPE_SYNC</b>, the bits should be interpreted as <b>DS_REPSYNC_*</b>. <b>ADD</b>, <b>DELETE</b>, <b>MODIFY</b>, and <b>UPDATE_REFS</b> use <b>DS_REPADD_*</b>, <b>DS_REPDEL_*</b>, <b>DS_REPMOD_*</b>, and <b>DS_REPUPD_*</b>. For more information, and descriptions of these bits, see 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasynca">DsReplicaSync</a>, 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaadda">DsReplicaAdd</a>, 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicadela">DsReplicaDel</a>, 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicamodifya">DsReplicaModify</a>, and 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa">DsReplicaUpdateRefs</a>.

Contains a set of flags that provide additional data about the operation. The contents of this member is determined by the contents of the <b>OpType</b> member.


This list describes the contents of the <i>ulOptions</i> parameter for each <i>OpType</i> value.





#### DS_REPL_OP_TYPE_SYNC

Contains zero or a combination of one or more of the <b>DS_REPSYNC_*</b> values as defined for the <i>Options</i> parameter in <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasynca">DsReplicaSync</a>.



#### DS_REPL_OP_TYPE_ADD

Contains zero or a combination of one or more of the <b>DS_REPADD_*</b> values as defined for the <i>Options</i> parameter in <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaadda">DsReplicaAdd</a>.



#### DS_REPL_OP_TYPE_DELETE

Contains zero or a combination of one or more of the <b>DS_REPDEL_*</b> values as defined for the <i>Options</i> parameter in <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicadela">DsReplicaDel</a>.



#### DS_REPL_OP_TYPE_MODIFY

Contains zero or a combination of one or more of the <b>DS_REPMOD_*</b> values as defined for the <i>Options</i> parameter in <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicamodifya">DsReplicaModify</a>.



#### DS_REPL_OP_TYPE_UPDATE_REFS

Contains zero or a combination of one or more of the <b>DS_REPSUPD_*</b> values as defined for the <i>Options</i> parameter in <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa">DsReplicaUpdateRefs</a>.

### -field oszNamingContext

Contains the offset, in bytes, from the address of this structure  to  a null-terminated string that contains the distinguished name of the naming context associated with this operation. For example, the naming context to be synchronized for <b>DS_REPL_OP_TYPE_SYNC</b>.

### -field oszDsaDN

Contains the offset, in bytes, from the address of this structure  to  a null-terminated string that contains the distinguished name of the directory system agent object associated with the remote server corresponding to this operation. For example, the server from which to ask for changes for <b>DS_REPL_OP_TYPE_SYNC</b>. This can be  <b>NULL</b>.

### -field oszDsaAddress

Contains the offset, in bytes, from the address of this structure  to  a null-terminated string that contains the transport-specific network address of the remote server associated with this operation. For example, the DNS or SMTP address of the server from which to ask for changes for <b>DS_REPL_OP_TYPE_SYNC</b>. This can be  <b>NULL</b>.

### -field uuidNamingContextObjGuid

Contains the <b>objectGuid</b> of the naming context identified by <b>pszNamingContext</b>.

### -field uuidDsaObjGuid

Contains the <b>objectGuid</b> of the directory system agent object identified by <b>pszDsaDN</b>.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_opw">DS_REPL_OP</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a>