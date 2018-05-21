---
UID: NS:ntdsapi._DS_REPL_OPW_BLOB
title: "_DS_REPL_OPW_BLOB"
author: windows-driver-content
description: The DS_REPL_OPW_BLOB structure describes a replication task currently executing or pending execution.
old-location: ad\ds_repl_opw_blob.htm
old-project: AD
ms.assetid: 14676159-cc31-4254-b174-dcd84d9ceec1
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: DS_REPL_OPW_BLOB, DS_REPL_OPW_BLOB structure [Active Directory], DS_REPL_OP_TYPE_ADD, DS_REPL_OP_TYPE_DELETE, DS_REPL_OP_TYPE_MODIFY, DS_REPL_OP_TYPE_SYNC, DS_REPL_OP_TYPE_UPDATE_REFS, _DS_REPL_OPW_BLOB, ad.ds_repl_opw_blob, ntdsapi/DS_REPL_OPW_BLOB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DS_REPL_OPW_BLOB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntdsapi.h
api_name:
-	DS_REPL_OPW_BLOB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _DS_REPL_OPW_BLOB structure


## -description


The <b>DS_REPL_OPW_BLOB</b> structure describes a replication task currently executing or pending execution. This structure is similar to the <a href="https://msdn.microsoft.com/9ea783b3-1529-4424-a582-f46f2a239a60">DS_REPL_OP</a> structure, but is obtained from the <a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-ReplPendingOps</b> attribute.


## -struct-fields




### -field ftimeEnqueued

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date and time that this operation was added to the queue.


### -field ulSerialNumber

Contains the identifier of the operation. This value is unique  in the startup routine of every computer. When the computer is restarted, the identifiers are no longer unique.


### -field ulPriority

Contains the priority value of this operation. Tasks with a higher priority value are executed first. The priority is calculated by the server based on the type of operation and its parameters.


### -field OpType

Contains one of the <a href="https://msdn.microsoft.com/81d9f464-90f4-405c-b014-0a61f5a5b816">DS_REPL_OP_TYPE</a> values that indicate the type of operation that this structure represents.


### -field ulOptions

Zero or more bits, the interpretation of which depends on the <b>OpType</b>. For <b>DS_REPL_OP_TYPE_SYNC</b>, the bits should be interpreted as <b>DS_REPSYNC_*</b>. <b>ADD</b>, <b>DELETE</b>, <b>MODIFY</b>, and <b>UPDATE_REFS</b> use <b>DS_REPADD_*</b>, <b>DS_REPDEL_*</b>, <b>DS_REPMOD_*</b>, and <b>DS_REPUPD_*</b>. For more information, and descriptions of these bits, see 
<a href="https://msdn.microsoft.com/20c7f96d-f298-4321-a6f5-910c25e418db">DsReplicaSync</a>, 
<a href="https://msdn.microsoft.com/33bd1b61-b9ed-479f-a128-fb7ddbb5e9af">DsReplicaAdd</a>, 
<a href="https://msdn.microsoft.com/68c767c4-bbb6-477b-8ffb-94f3ae235375">DsReplicaDel</a>, 
<a href="https://msdn.microsoft.com/aad20527-1211-41bc-b0e9-02e4ab28ae2e">DsReplicaModify</a>, and 
<a href="https://msdn.microsoft.com/158c7e73-0e6c-4b71-a87f-2f60f3db91cb">DsReplicaUpdateRefs</a>.

Contains a set of flags that provide additional data about the operation. The contents of this member is determined by the contents of the <b>OpType</b> member.


This list describes the contents of the <i>ulOptions</i> parameter for each <i>OpType</i> value.





#### DS_REPL_OP_TYPE_SYNC

Contains zero or a combination of one or more of the <b>DS_REPSYNC_*</b> values as defined for the <i>Options</i> parameter in <a href="https://msdn.microsoft.com/20c7f96d-f298-4321-a6f5-910c25e418db">DsReplicaSync</a>.



#### DS_REPL_OP_TYPE_ADD

Contains zero or a combination of one or more of the <b>DS_REPADD_*</b> values as defined for the <i>Options</i> parameter in <a href="https://msdn.microsoft.com/33bd1b61-b9ed-479f-a128-fb7ddbb5e9af">DsReplicaAdd</a>.



#### DS_REPL_OP_TYPE_DELETE

Contains zero or a combination of one or more of the <b>DS_REPDEL_*</b> values as defined for the <i>Options</i> parameter in <a href="https://msdn.microsoft.com/68c767c4-bbb6-477b-8ffb-94f3ae235375">DsReplicaDel</a>.



#### DS_REPL_OP_TYPE_MODIFY

Contains zero or a combination of one or more of the <b>DS_REPMOD_*</b> values as defined for the <i>Options</i> parameter in <a href="https://msdn.microsoft.com/aad20527-1211-41bc-b0e9-02e4ab28ae2e">DsReplicaModify</a>.



#### DS_REPL_OP_TYPE_UPDATE_REFS

Contains zero or a combination of one or more of the <b>DS_REPSUPD_*</b> values as defined for the <i>Options</i> parameter in <a href="https://msdn.microsoft.com/158c7e73-0e6c-4b71-a87f-2f60f3db91cb">DsReplicaUpdateRefs</a>.


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




<a href="https://msdn.microsoft.com/9ea783b3-1529-4424-a582-f46f2a239a60">DS_REPL_OP</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a>
 

 

