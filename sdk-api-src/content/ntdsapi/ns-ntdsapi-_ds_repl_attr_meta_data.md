---
UID: NS:ntdsapi._DS_REPL_ATTR_META_DATA
title: "_DS_REPL_ATTR_META_DATA"
author: windows-sdk-content
description: The DS_REPL_ATTR_META_DATA structure is used with the DsReplicaGetInfo and DsReplicaGetInfo2 functions to contain replication state data for an object attribute.
old-location: ad\ds_repl_attr_meta_data.htm
old-project: ad
ms.assetid: 27ccc1c9-03d7-4d13-b9ec-65d6b8bdfd37
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DS_REPL_ATTR_META_DATA, DS_REPL_ATTR_META_DATA structure [Active Directory], _DS_REPL_ATTR_META_DATA, _glines_ds_repl_attr_meta_data, ad.ds__repl__attr__meta__data, ad.ds_repl_attr_meta_data, ntdsapi/DS_REPL_ATTR_META_DATA
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
req.typenames: DS_REPL_ATTR_META_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_ATTR_META_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _DS_REPL_ATTR_META_DATA structure


## -description


The <b>DS_REPL_ATTR_META_DATA</b> structure is used with the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions to contain replication state data for an object attribute.


## -struct-fields




### -field pszAttributeName

Pointer to a null-terminated Unicode string that contains the LDAP display name of the attribute corresponding to this metadata.


### -field dwVersion

Contains the version of this attribute. Each originating modification of the attribute increases this value by one. Replication of a modification does not affect the version.


### -field ftimeLastOriginatingChange

Contains the time at which the last originating change was made to this attribute. Replication of the change does not affect this value.


### -field uuidLastOriginatingDsaInvocationID

Contains the invocation identification of the server on which the last change was made to this attribute. Replication of the change does not affect this value.


### -field usnOriginatingChange

Contains the update sequence number (USN) on the originating server at which the last change to this attribute was made. Replication of the change does not affect this value.


### -field usnLocalChange

Contains the USN on the destination server (the server from which the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> function retrieved the metadata) at which the last change to this attribute was applied. This value typically is different on all servers.


## -see-also




<a href="https://msdn.microsoft.com/7851ffbc-5d05-4ea7-b3b4-1b8b77299be5">DS_REPL_OBJ_META_DATA</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

