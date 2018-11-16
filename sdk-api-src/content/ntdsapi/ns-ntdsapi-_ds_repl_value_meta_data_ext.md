---
UID: NS:ntdsapi._DS_REPL_VALUE_META_DATA_EXT
title: "_DS_REPL_VALUE_META_DATA_EXT"
author: windows-sdk-content
description: Contains attribute replication meta data for the DS_REPL_ATTR_VALUE_META_DATA_EXT structure.
old-location: ad\ds_repl_value_meta_data_ext.htm
tech.root: ad
ms.assetid: 2BE0F9C4-D688-4DE6-8DB2-15666D8BD070
ms.author: windowssdkdev
ms.date: 11/14/2018
ms.keywords: DS_REPL_VALUE_META_DATA_EXT, DS_REPL_VALUE_META_DATA_EXT structure [Active Directory], PDS_REPL_VALUE_META_DATA_EXT, PDS_REPL_VALUE_META_DATA_EXT structure pointer [Active Directory], _DS_REPL_VALUE_META_DATA_EXT, ad.ds_repl_value_meta_data_ext, ntdsapi/DS_REPL_VALUE_META_DATA_EXT, ntdsapi/PDS_REPL_VALUE_META_DATA_EXT
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
 - DS_REPL_VALUE_META_DATA_EXT
product: Windows
targetos: Windows
req.typenames: DS_REPL_VALUE_META_DATA_EXT
req.redist: 
---

# _DS_REPL_VALUE_META_DATA_EXT structure


## -description


Contains attribute replication meta data for the <a href="https://msdn.microsoft.com/CA41C6BF-A485-4AC7-B761-3A07159C2FF1">DS_REPL_ATTR_VALUE_META_DATA_EXT</a> structure.


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

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time this attribute was deleted.


### -field ftimeCreated

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time this attribute was created.


### -field dwVersion

Contains the version of this attribute. Each originating modification of the attribute increases this value by one. Replication of a modification does not affect the version.


### -field ftimeLastOriginatingChange

Contains a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time at which the last originating change was made to this attribute. Replication of the change does not affect this value.


### -field uuidLastOriginatingDsaInvocationID

Contains the invocation identifier of the server on which the last change was made to this attribute. Replication of the change does not affect this value.


### -field usnOriginatingChange

Contains the update sequence number (USN) on the originating server at which the last change to this attribute was made. Replication of the change does not affect this value.


### -field usnLocalChange

Contains the USN on the destination server, that is the server from which the <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function retrieved the metadata, at which the last change to this attribute was applied. This value is typically different on all servers.


### -field pszLastOriginatingDsaDN

Pointer to a null-terminated Unicode string that contains the distinguished name of the directory system agent server that originated the last replication.


### -field dwUserIdentifier

TBD


### -field dwPriorLinkState

TBD


### -field dwCurrentLinkState

TBD

