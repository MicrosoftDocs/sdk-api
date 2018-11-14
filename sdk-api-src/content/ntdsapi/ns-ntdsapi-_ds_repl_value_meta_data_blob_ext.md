---
UID: NS:ntdsapi._DS_REPL_VALUE_META_DATA_BLOB_EXT
title: "_DS_REPL_VALUE_META_DATA_BLOB_EXT"
author: windows-sdk-content
description: Contains attribute value replication metadata.
old-location: ad\ds_repl_value_meta_data_blob_ext.htm
tech.root: ad
ms.assetid: 095180F4-9E3F-47EE-B39E-107D7D219DCB
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DS_REPL_VALUE_META_DATA_BLOB_EXT, DS_REPL_VALUE_META_DATA_BLOB_EXT structure [Active Directory], _DS_REPL_VALUE_META_DATA_BLOB_EXT, ad.ds_repl_value_meta_data_blob_ext, ntdsapi/DS_REPL_VALUE_META_DATA_BLOB_EXT
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - DS_REPL_VALUE_META_DATA_BLOB_EXT
product: Windows
targetos: Windows
req.typenames: DS_REPL_VALUE_META_DATA_BLOB_EXT
req.redist: 
---

# _DS_REPL_VALUE_META_DATA_BLOB_EXT structure


## -description


Contains attribute value replication metadata. This structure is similar to the <a href="https://msdn.microsoft.com/2BE0F9C4-D688-4DE6-8DB2-15666D8BD070">DS_REPL_VALUE_META_DATA_EXT</a> structure, but is obtained from the <a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-ReplValueMetaData</b> attribute.


## -struct-fields




### -field oszAttributeName

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the LDAP display name of the attribute corresponding to this metadata. A value of zero indicates an empty or <b>NULL</b> string.


### -field oszObjectDn

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the distinguished name of the object that this attribute belongs to. A value of zero indicates an empty or <b>NULL</b> string.


### -field cbData

Contains the number of bytes in the <b>pbData</b> array.


### -field obData

Pointer to a buffer that contains the attribute replication metadata. The <b>cbData</b> member contains the length, in bytes, of this buffer.


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


### -field dwUserIdentifier

TBD


### -field dwPriorLinkState

TBD


### -field dwCurrentLinkState

TBD


## -see-also




<a href="https://msdn.microsoft.com/42b20d3b-1799-4f5f-b74e-fe9284dd8ac3">Domain Controller and Replication Management Structures</a>



<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/32bc9909-e476-423c-bbb5-3978234457fd">Lightweight Directory Access Protocol API</a>
 

 

