---
UID: NS:ntdsapi._DS_REPL_ATTR_META_DATA_2
title: DS_REPL_ATTR_META_DATA_2 (ntdsapi.h)
description: The DS_REPL_ATTR_META_DATA_2 structure is used with the DsReplicaGetInfo and DsReplicaGetInfo2 functions to contain replication state data for an object attribute.helpviewer_keywords: ["DS_REPL_ATTR_META_DATA_2","DS_REPL_ATTR_META_DATA_2 structure [Active Directory]","ad.ds_repl_attr_meta_data_2","ntdsapi/DS_REPL_ATTR_META_DATA_2"]
old-location: ad\ds_repl_attr_meta_data_2.htm
tech.root: ad
ms.assetid: 392457b7-df69-44d0-82b2-8381d5877354
ms.date: 12/05/2018
ms.keywords: DS_REPL_ATTR_META_DATA_2, DS_REPL_ATTR_META_DATA_2 structure [Active Directory], ad.ds_repl_attr_meta_data_2, ntdsapi/DS_REPL_ATTR_META_DATA_2
f1_keywords:
- ntdsapi/DS_REPL_ATTR_META_DATA_2
dev_langs:
- c++
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
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ntdsapi.h
api_name:
- DS_REPL_ATTR_META_DATA_2
targetos: Windows
req.typenames: DS_REPL_ATTR_META_DATA_2
req.redist: 
ms.custom: 19H1
---

# DS_REPL_ATTR_META_DATA_2 structure


## -description


The <b>DS_REPL_ATTR_META_DATA_2</b> structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> functions to contain replication state data for an object attribute.


## -struct-fields




### -field pszAttributeName

Pointer to a null-terminated Unicode string that contains the LDAP display name of the attribute that corresponds to this metadata.


### -field dwVersion

Contains the version of this attribute. Each originating modification of the attribute increases this value by one. Replication of a modification does not affect the version.


### -field ftimeLastOriginatingChange

Contains the time at which the last originating change was made to this attribute. Replication of the change does not affect this value.


### -field uuidLastOriginatingDsaInvocationID

Contains the invocation identification of the server on which the last change was made to this attribute. Replication of the change does not affect this value.


### -field usnOriginatingChange

Contains the update sequence number (USN) on the originating server at which the last change to this attribute was made. Replication of the change does not affect this value.


### -field usnLocalChange

Contains the USN on the destination server (the server from which the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> function retrieved the metadata) at which the last change to this attribute was applied. This value typically is different on all servers.


### -field pszLastOriginatingDsaDN

Pointer to a null-terminated Unicode string that contains the distinguished name of the directory system agent server that originated the last replication.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2">DS_REPL_OBJ_META_DATA_2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>
 

 

