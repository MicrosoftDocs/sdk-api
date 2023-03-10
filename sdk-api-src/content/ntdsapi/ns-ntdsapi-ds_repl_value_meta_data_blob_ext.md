---
UID: NS:ntdsapi._DS_REPL_VALUE_META_DATA_BLOB_EXT
title: DS_REPL_VALUE_META_DATA_BLOB_EXT (ntdsapi.h)
description: Contains attribute value replication metadata.
helpviewer_keywords: ["DS_REPL_VALUE_META_DATA_BLOB_EXT","DS_REPL_VALUE_META_DATA_BLOB_EXT structure [Active Directory]","ad.ds_repl_value_meta_data_blob_ext","ntdsapi/DS_REPL_VALUE_META_DATA_BLOB_EXT"]
old-location: ad\ds_repl_value_meta_data_blob_ext.htm
tech.root: ad
ms.assetid: 095180F4-9E3F-47EE-B39E-107D7D219DCB
ms.date: 12/05/2018
ms.keywords: DS_REPL_VALUE_META_DATA_BLOB_EXT, DS_REPL_VALUE_META_DATA_BLOB_EXT structure [Active Directory], ad.ds_repl_value_meta_data_blob_ext, ntdsapi/DS_REPL_VALUE_META_DATA_BLOB_EXT
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
req.typenames: DS_REPL_VALUE_META_DATA_BLOB_EXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_VALUE_META_DATA_BLOB_EXT
 - ntdsapi/_DS_REPL_VALUE_META_DATA_BLOB_EXT
 - DS_REPL_VALUE_META_DATA_BLOB_EXT
 - ntdsapi/DS_REPL_VALUE_META_DATA_BLOB_EXT
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - DS_REPL_VALUE_META_DATA_BLOB_EXT
---

# DS_REPL_VALUE_META_DATA_BLOB_EXT structure


## -description

Contains attribute value replication metadata. This structure is similar to the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext">DS_REPL_VALUE_META_DATA_EXT</a> structure, but is obtained from the <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-ReplValueMetaData</b> attribute.

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

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time that  this attribute was deleted.

### -field ftimeCreated

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time that this attribute was created.

### -field dwVersion

Contains the version of this attribute. Each originating modification of the attribute increases this value by one. Replication of a modification does not affect the version.

### -field ftimeLastOriginatingChange

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time at which the last originating change was made to this attribute. Replication of the change does not affect this value.

### -field uuidLastOriginatingDsaInvocationID

Contains the invocation identifier of the server on which the last change was made to this attribute. Replication of the change does not affect this value.

### -field usnOriginatingChange

Contains the update sequence number (USN) on the originating server at which the last change to this attribute was made. Replication of the change does not affect this value.

### -field usnLocalChange

Contains the USN on the destination server, that is, the server from which the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function retrieved the metadata, at which the last change to this attribute was applied. This value is typically different on all servers.

### -field oszLastOriginatingDsaDN

Contains the offset, in bytes, from the address of this structure  to  a null-terminated Unicode string that contains the distinguished name of the directory system agent server that originated the last replication. A value of zero indicates an empty or <b>NULL</b> string.

### -field dwUserIdentifier

TBD

### -field dwPriorLinkState

TBD

### -field dwCurrentLinkState

TBD

## -see-also

<a href="/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a>