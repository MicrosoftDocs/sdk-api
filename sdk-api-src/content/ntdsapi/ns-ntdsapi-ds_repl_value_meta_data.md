---
UID: NS:ntdsapi._DS_REPL_VALUE_META_DATA
title: DS_REPL_VALUE_META_DATA (ntdsapi.h)
description: Used with the DS_REPL_ATTR_VALUE_META_DATA structure to contain attribute value replication metadata.
helpviewer_keywords: ["DS_REPL_VALUE_META_DATA","DS_REPL_VALUE_META_DATA structure [Active Directory]","ad.ds_repl_value_meta_data","ntdsapi/DS_REPL_VALUE_META_DATA"]
old-location: ad\ds_repl_value_meta_data.htm
tech.root: ad
ms.assetid: 294a466e-8a83-4b33-a8a8-ac7b51d081d4
ms.date: 12/05/2018
ms.keywords: DS_REPL_VALUE_META_DATA, DS_REPL_VALUE_META_DATA structure [Active Directory], ad.ds_repl_value_meta_data, ntdsapi/DS_REPL_VALUE_META_DATA
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
req.typenames: DS_REPL_VALUE_META_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_VALUE_META_DATA
 - ntdsapi/_DS_REPL_VALUE_META_DATA
 - DS_REPL_VALUE_META_DATA
 - ntdsapi/DS_REPL_VALUE_META_DATA
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
 - DS_REPL_VALUE_META_DATA
---

# DS_REPL_VALUE_META_DATA structure


## -description

The <b>DS_REPL_VALUE_META_DATA</b> structure is used with the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data">DS_REPL_ATTR_VALUE_META_DATA</a> structure to contain attribute value replication metadata.

## -struct-fields

### -field pszAttributeName

Pointer to a null-terminated Unicode string that contains the LDAP display name of the attribute corresponding to this metadata.

### -field pszObjectDn

Pointer to a null-terminated Unicode string that contains the distinguished name of the object that this attribute belongs to.

### -field cbData

Contains the number of bytes in the <b>pbData</b> array.

### -field pbData.size_is

### -field pbData.size_is.cbData

### -field pbData.ptr

### -field pbData

Pointer to a buffer that contains the attribute replication metadata. The <b>cbData</b> member contains the length, in bytes, of this buffer.

### -field ftimeDeleted

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time this attribute was deleted.

### -field ftimeCreated

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time this attribute was created.

### -field dwVersion

Contains the version of this attribute. Each originating modification of the attribute increases this value by one. Replication of a modification does not affect the version.

### -field ftimeLastOriginatingChange

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time at which the last originating change was made to this attribute. Replication of the change does not affect this value.

### -field uuidLastOriginatingDsaInvocationID

Contains the invocation identifier of the server on which the last change was made to this attribute. Replication of the change does not affect this value.

### -field usnOriginatingChange

Contains the update sequence number (USN) on the originating server at which the last change to this attribute was made. Replication of the change does not affect this value.

### -field usnLocalChange

Contains the USN on the destination server, that is the server from which the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function retrieved the metadata, at which the last change to this attribute was applied. This value is typically different on all servers.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data">DS_REPL_ATTR_VALUE_META_DATA</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>