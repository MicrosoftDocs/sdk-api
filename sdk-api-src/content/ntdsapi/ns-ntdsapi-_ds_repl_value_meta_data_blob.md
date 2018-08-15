---
UID: NS:ntdsapi._DS_REPL_VALUE_META_DATA_BLOB
title: "_DS_REPL_VALUE_META_DATA_BLOB"
author: windows-sdk-content
description: Used to contain attribute value replication metadata.
old-location: ad\ds_repl_value_meta_data_blob.htm
old-project: ad
ms.assetid: 7d8bb666-c5d8-43de-ab72-5b02b6e0593d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DS_REPL_VALUE_META_DATA_BLOB, DS_REPL_VALUE_META_DATA_BLOB structure [Active Directory], _DS_REPL_VALUE_META_DATA_BLOB, ad.ds_repl_value_meta_data_blob, ntdsapi/DS_REPL_VALUE_META_DATA_BLOB
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntdsapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DS_REPL_VALUE_META_DATA_BLOB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_VALUE_META_DATA_BLOB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _DS_REPL_VALUE_META_DATA_BLOB structure


## -description


The <b>DS_REPL_VALUE_META_DATA_BLOB</b> structure is used to contain attribute value replication metadata. This structure is similar to the <a href="https://msdn.microsoft.com/747e32b8-2cc0-4fcd-88dc-027188598361">DS_REPL_VALUE_META_DATA_2</a> structure, but is obtained from the <a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-ReplValueMetaData</b> attribute.


## -struct-fields




### -field oszAttributeName

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the LDAP display name of the attribute corresponding to this metadata. A value of zero indicates an empty or <b>NULL</b> string.


### -field oszObjectDn

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the distinguished name of the object that this attribute belongs to. A value of zero indicates an empty or <b>NULL</b> string.


### -field cbData

Contains the number of bytes in the <b>pbData</b> array.


### -field obData

 


### -field ftimeDeleted

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time that  this attribute was deleted.


### -field ftimeCreated

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time that this attribute was created.


### -field dwVersion

Contains the version of this attribute. Each originating modification of the attribute increases this value by one. Replication of a modification does not affect the version.


### -field ftimeLastOriginatingChange

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time at which the last originating change was made to this attribute. Replication of the change does not affect this value.


### -field uuidLastOriginatingDsaInvocationID

Contains the invocation identifier of the server on which the last change was made to this attribute. Replication of the change does not affect this value.


### -field usnOriginatingChange

Contains the update sequence number (USN) on the originating server at which the last change to this attribute was made. Replication of the change does not affect this value.


### -field usnLocalChange

Contains the USN on the destination server, that is, the server from which the <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function retrieved the metadata, at which the last change to this attribute was applied. This value is typically different on all servers.


### -field oszLastOriginatingDsaDN

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the distinguished name of the directory system agent server that originated the last replication. A value of zero indicates an empty or <b>NULL</b> string.


#### - pbData

Pointer to a buffer that contains the attribute replication metadata. The <b>cbData</b> member contains the length, in bytes, of this buffer.


## -see-also




<a href="https://msdn.microsoft.com/747e32b8-2cc0-4fcd-88dc-027188598361">DS_REPL_VALUE_META_DATA_2</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a>
 

 

