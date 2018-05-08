---
UID: NS:ntdsapi._DS_REPL_ATTR_META_DATA_2
title: "_DS_REPL_ATTR_META_DATA_2"
author: windows-driver-content
description: The DS_REPL_ATTR_META_DATA_2 structure is used with the DsReplicaGetInfo and DsReplicaGetInfo2 functions to contain replication state data for an object attribute.
old-location: ad\ds_repl_attr_meta_data_2.htm
old-project: AD
ms.assetid: 392457b7-df69-44d0-82b2-8381d5877354
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: DS_REPL_ATTR_META_DATA_2, DS_REPL_ATTR_META_DATA_2 structure [Active Directory], _DS_REPL_ATTR_META_DATA_2, ad.ds_repl_attr_meta_data_2, ntdsapi/DS_REPL_ATTR_META_DATA_2
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
req.typenames: DS_REPL_ATTR_META_DATA_2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntdsapi.h
api_name:
-	DS_REPL_ATTR_META_DATA_2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _DS_REPL_ATTR_META_DATA_2 structure


## -description


The <b>DS_REPL_ATTR_META_DATA_2</b> structure is used with the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions to contain replication state data for an object attribute.


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

Contains the USN on the destination server (the server from which the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> function retrieved the metadata) at which the last change to this attribute was applied. This value typically is different on all servers.


### -field pszLastOriginatingDsaDN

Pointer to a null-terminated Unicode string that contains the distinguished name of the directory system agent server that originated the last replication.


## -see-also




<a href="https://msdn.microsoft.com/2aed753f-432c-4de8-a6be-aa79833f002f">DS_REPL_OBJ_META_DATA_2</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

