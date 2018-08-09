---
UID: NE:ntdsapi._DS_REPL_INFO_TYPE
title: "_DS_REPL_INFO_TYPE"
author: windows-sdk-content
description: The DS_REPL_INFO_TYPE enumeration is used with the DsReplicaGetInfo and DsReplicaGetInfo2 functions to specify the type of replication data to retrieve.
old-location: ad\ds_repl_info_type.htm
old-project: ad
ms.assetid: 88d8a164-2192-4e73-a190-aa5b5dbb1101
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DS_REPL_INFO_CURSORS_2_FOR_NC, DS_REPL_INFO_CURSORS_3_FOR_NC, DS_REPL_INFO_CURSORS_FOR_NC, DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES, DS_REPL_INFO_KCC_DSA_LINK_FAILURES, DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE, DS_REPL_INFO_METADATA_2_FOR_OBJ, DS_REPL_INFO_METADATA_FOR_ATTR_VALUE, DS_REPL_INFO_METADATA_FOR_OBJ, DS_REPL_INFO_NEIGHBORS, DS_REPL_INFO_PENDING_OPS, DS_REPL_INFO_TYPE, DS_REPL_INFO_TYPE enumeration [Active Directory], _DS_REPL_INFO_TYPE, _glines_ds_repl_info_type, ad.ds__repl__info__type, ad.ds_repl_info_type, ntdsapi/DS_REPL_INFO_CURSORS_2_FOR_NC, ntdsapi/DS_REPL_INFO_CURSORS_3_FOR_NC, ntdsapi/DS_REPL_INFO_CURSORS_FOR_NC, ntdsapi/DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES, ntdsapi/DS_REPL_INFO_KCC_DSA_LINK_FAILURES, ntdsapi/DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE, ntdsapi/DS_REPL_INFO_METADATA_2_FOR_OBJ, ntdsapi/DS_REPL_INFO_METADATA_FOR_ATTR_VALUE, ntdsapi/DS_REPL_INFO_METADATA_FOR_OBJ, ntdsapi/DS_REPL_INFO_NEIGHBORS, ntdsapi/DS_REPL_INFO_PENDING_OPS, ntdsapi/DS_REPL_INFO_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: DS_REPL_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_INFO_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: Any level
req.product: Rights Management Services client 1.0 or later
---

# _DS_REPL_INFO_TYPE enumeration


## -description


The <b>DS_REPL_INFO_TYPE</b> enumeration is used with the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions to  specify the type of replication data to retrieve.


## -enum-fields




### -field DS_REPL_INFO_NEIGHBORS

Requests replication state data for naming context and source server pairs. Returns a pointer to a 
<a href="https://msdn.microsoft.com/1307399b-de29-43ec-97b4-05cd70c1a92d">DS_REPL_NEIGHBORS</a> structure.


### -field DS_REPL_INFO_CURSORS_FOR_NC

Requests replication state data with respect to all replicas of a given naming context. Returns a pointer to a 
<a href="https://msdn.microsoft.com/0fe5ad72-d3f3-42a8-a36f-ca1fc9c55c50">DS_REPL_CURSORS</a> structure.


### -field DS_REPL_INFO_METADATA_FOR_OBJ

Requests replication state data for the attributes for the given object. Returns a pointer to a 
<a href="https://msdn.microsoft.com/7851ffbc-5d05-4ea7-b3b4-1b8b77299be5">DS_REPL_OBJ_META_DATA</a> structure.


### -field DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES

Requests replication state data with respect to connection failures between inbound replication partners. Returns a pointer to a 
<a href="https://msdn.microsoft.com/bb011502-38ae-43b7-a6ad-de16b499f61b">DS_REPL_KCC_DSA_FAILURES</a> structure.


### -field DS_REPL_INFO_KCC_DSA_LINK_FAILURES

Requests replication state data with respect to link failures between inbound replication partners. Returns a pointer to a 
<a href="https://msdn.microsoft.com/bb011502-38ae-43b7-a6ad-de16b499f61b">DS_REPL_KCC_DSA_FAILURES</a> structure.


### -field DS_REPL_INFO_PENDING_OPS

Requests the replication tasks currently executing or queued to execute. Returns a pointer to a 
<a href="https://msdn.microsoft.com/2e4b96cb-fbd6-496b-aff3-cb7d82f1fa39">DS_REPL_PENDING_OPS</a> structure.


### -field DS_REPL_INFO_METADATA_FOR_ATTR_VALUE

Requests replication state data for a specific attribute for the given object. Returns a pointer to a 
<a href="https://msdn.microsoft.com/b13cdd31-d154-4539-81d6-d7a449e2b3d5">DS_REPL_ATTR_VALUE_META_DATA</a> structure.


### -field DS_REPL_INFO_CURSORS_2_FOR_NC

Requests replication state data with respect to all replicas of a given naming context. Returns a pointer to a 
<a href="https://msdn.microsoft.com/5a1981ac-3b6a-4e48-8430-f8297ddd3283">DS_REPL_CURSORS_2</a> structure.


### -field DS_REPL_INFO_CURSORS_3_FOR_NC

Requests replication state data with respect to all replicas of a given naming context. Returns a pointer to a 
<a href="https://msdn.microsoft.com/7b8e0015-dd8f-4cba-8ea2-683cb107f294">DS_REPL_CURSORS_3</a> structure.


### -field DS_REPL_INFO_METADATA_2_FOR_OBJ

Requests replication state data for the attributes for the given object. Returns a pointer to a 
<a href="https://msdn.microsoft.com/2aed753f-432c-4de8-a6be-aa79833f002f">DS_REPL_OBJ_META_DATA_2</a> structure.


### -field DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE

Requests replication state data for a specific attribute for the given object. Returns a pointer to a 
<a href="https://msdn.microsoft.com/2022362a-e2f7-4cfd-a512-cfe29e5d439d">DS_REPL_ATTR_VALUE_META_DATA_2</a> structure.


### -field DS_REPL_INFO_METADATA_EXT_FOR_ATTR_VALUE


### -field DS_REPL_INFO_TYPE_MAX




## -see-also




<a href="https://msdn.microsoft.com/27ccc1c9-03d7-4d13-b9ec-65d6b8bdfd37">DS_REPL_ATTR_VALUE_META_DATA</a>



<a href="https://msdn.microsoft.com/392457b7-df69-44d0-82b2-8381d5877354">DS_REPL_ATTR_VALUE_META_DATA_2</a>



<a href="https://msdn.microsoft.com/0fe5ad72-d3f3-42a8-a36f-ca1fc9c55c50">DS_REPL_CURSORS</a>



<a href="https://msdn.microsoft.com/5a1981ac-3b6a-4e48-8430-f8297ddd3283">DS_REPL_CURSORS_2</a>



<a href="https://msdn.microsoft.com/7b8e0015-dd8f-4cba-8ea2-683cb107f294">DS_REPL_CURSORS_3</a>



<a href="https://msdn.microsoft.com/bb011502-38ae-43b7-a6ad-de16b499f61b">DS_REPL_KCC_DSA_FAILURES</a>



<a href="https://msdn.microsoft.com/1307399b-de29-43ec-97b4-05cd70c1a92d">DS_REPL_NEIGHBORS</a>



<a href="https://msdn.microsoft.com/7851ffbc-5d05-4ea7-b3b4-1b8b77299be5">DS_REPL_OBJ_META_DATA</a>



<a href="https://msdn.microsoft.com/2aed753f-432c-4de8-a6be-aa79833f002f">DS_REPL_OBJ_META_DATA_2</a>



<a href="https://msdn.microsoft.com/2e4b96cb-fbd6-496b-aff3-cb7d82f1fa39">DS_REPL_PENDING_OPS</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

