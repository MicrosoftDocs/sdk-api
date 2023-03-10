---
UID: NS:ntdsapi._DS_REPL_VALUE_META_DATA_EXT
title: DS_REPL_VALUE_META_DATA_EXT (ntdsapi.h)
description: Contains attribute replication meta data for the DS_REPL_ATTR_VALUE_META_DATA_EXT structure.
helpviewer_keywords: ["DS_REPL_VALUE_META_DATA_EXT","DS_REPL_VALUE_META_DATA_EXT structure [Active Directory]","PDS_REPL_VALUE_META_DATA_EXT","PDS_REPL_VALUE_META_DATA_EXT structure pointer [Active Directory]","ad.ds_repl_value_meta_data_ext","ntdsapi/DS_REPL_VALUE_META_DATA_EXT","ntdsapi/PDS_REPL_VALUE_META_DATA_EXT"]
old-location: ad\ds_repl_value_meta_data_ext.htm
tech.root: ad
ms.assetid: 2BE0F9C4-D688-4DE6-8DB2-15666D8BD070
ms.date: 12/05/2018
ms.keywords: DS_REPL_VALUE_META_DATA_EXT, DS_REPL_VALUE_META_DATA_EXT structure [Active Directory], PDS_REPL_VALUE_META_DATA_EXT, PDS_REPL_VALUE_META_DATA_EXT structure pointer [Active Directory], ad.ds_repl_value_meta_data_ext, ntdsapi/DS_REPL_VALUE_META_DATA_EXT, ntdsapi/PDS_REPL_VALUE_META_DATA_EXT
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
req.typenames: DS_REPL_VALUE_META_DATA_EXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_VALUE_META_DATA_EXT
 - ntdsapi/_DS_REPL_VALUE_META_DATA_EXT
 - DS_REPL_VALUE_META_DATA_EXT
 - ntdsapi/DS_REPL_VALUE_META_DATA_EXT
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - DS_REPL_VALUE_META_DATA_EXT
---

# DS_REPL_VALUE_META_DATA_EXT structure


## -description

Contains attribute replication meta data for the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext">DS_REPL_ATTR_VALUE_META_DATA_EXT</a> structure.

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

### -field pszLastOriginatingDsaDN

Pointer to a null-terminated Unicode string that contains the distinguished name of the directory system agent server that originated the last replication.

### -field dwUserIdentifier

TBD

### -field dwPriorLinkState

TBD

### -field dwCurrentLinkState

TBD