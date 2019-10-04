---
UID: NE:ntdsapi._DS_REPL_INFO_TYPE
title: DS_REPL_INFO_TYPE (ntdsapi.h)
author: windows-sdk-content
description: The DS_REPL_INFO_TYPE enumeration is used with the DsReplicaGetInfo and DsReplicaGetInfo2 functions to specify the type of replication data to retrieve.
old-location: ad\ds_repl_info_type.htm
tech.root: ad
ms.assetid: 88d8a164-2192-4e73-a190-aa5b5dbb1101
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DS_REPL_INFO_CURSORS_2_FOR_NC, DS_REPL_INFO_CURSORS_3_FOR_NC, DS_REPL_INFO_CURSORS_FOR_NC, DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES, DS_REPL_INFO_KCC_DSA_LINK_FAILURES, DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE, DS_REPL_INFO_METADATA_2_FOR_OBJ, DS_REPL_INFO_METADATA_FOR_ATTR_VALUE, DS_REPL_INFO_METADATA_FOR_OBJ, DS_REPL_INFO_NEIGHBORS, DS_REPL_INFO_PENDING_OPS, DS_REPL_INFO_TYPE, DS_REPL_INFO_TYPE enumeration [Active Directory], _glines_ds_repl_info_type, ad.ds__repl__info__type, ad.ds_repl_info_type, ntdsapi/DS_REPL_INFO_CURSORS_2_FOR_NC, ntdsapi/DS_REPL_INFO_CURSORS_3_FOR_NC, ntdsapi/DS_REPL_INFO_CURSORS_FOR_NC, ntdsapi/DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES, ntdsapi/DS_REPL_INFO_KCC_DSA_LINK_FAILURES, ntdsapi/DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE, ntdsapi/DS_REPL_INFO_METADATA_2_FOR_OBJ, ntdsapi/DS_REPL_INFO_METADATA_FOR_ATTR_VALUE, ntdsapi/DS_REPL_INFO_METADATA_FOR_OBJ, ntdsapi/DS_REPL_INFO_NEIGHBORS, ntdsapi/DS_REPL_INFO_PENDING_OPS, ntdsapi/DS_REPL_INFO_TYPE
ms.topic: enum
f1_keywords:
- ntdsapi/DS_REPL_INFO_TYPE
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
- DS_REPL_INFO_TYPE
targetos: Windows
req.typenames: DS_REPL_INFO_TYPE
req.redist: 
ms.custom: 19H1
---

# DS_REPL_INFO_TYPE enumeration


## -description


The <b>DS_REPL_INFO_TYPE</b> enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> functions to  specify the type of replication data to retrieve.


## -enum-fields




### -field DS_REPL_INFO_NEIGHBORS

Requests replication state data for naming context and source server pairs. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_neighborsw">DS_REPL_NEIGHBORS</a> structure.


### -field DS_REPL_INFO_CURSORS_FOR_NC

Requests replication state data with respect to all replicas of a given naming context. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursors">DS_REPL_CURSORS</a> structure.


### -field DS_REPL_INFO_METADATA_FOR_OBJ

Requests replication state data for the attributes for the given object. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data">DS_REPL_OBJ_META_DATA</a> structure.


### -field DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES

Requests replication state data with respect to connection failures between inbound replication partners. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw">DS_REPL_KCC_DSA_FAILURES</a> structure.


### -field DS_REPL_INFO_KCC_DSA_LINK_FAILURES

Requests replication state data with respect to link failures between inbound replication partners. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw">DS_REPL_KCC_DSA_FAILURES</a> structure.


### -field DS_REPL_INFO_PENDING_OPS

Requests the replication tasks currently executing or queued to execute. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_pending_opsw">DS_REPL_PENDING_OPS</a> structure.


### -field DS_REPL_INFO_METADATA_FOR_ATTR_VALUE

Requests replication state data for a specific attribute for the given object. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data">DS_REPL_ATTR_VALUE_META_DATA</a> structure.


### -field DS_REPL_INFO_CURSORS_2_FOR_NC

Requests replication state data with respect to all replicas of a given naming context. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursors_2">DS_REPL_CURSORS_2</a> structure.


### -field DS_REPL_INFO_CURSORS_3_FOR_NC

Requests replication state data with respect to all replicas of a given naming context. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursors_3w">DS_REPL_CURSORS_3</a> structure.


### -field DS_REPL_INFO_METADATA_2_FOR_OBJ

Requests replication state data for the attributes for the given object. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2">DS_REPL_OBJ_META_DATA_2</a> structure.


### -field DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE

Requests replication state data for a specific attribute for the given object. Returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2">DS_REPL_ATTR_VALUE_META_DATA_2</a> structure.


### -field DS_REPL_INFO_METADATA_EXT_FOR_ATTR_VALUE


### -field DS_REPL_INFO_TYPE_MAX




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data">DS_REPL_ATTR_VALUE_META_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2">DS_REPL_ATTR_VALUE_META_DATA_2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursors">DS_REPL_CURSORS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursors_2">DS_REPL_CURSORS_2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_cursors_3w">DS_REPL_CURSORS_3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw">DS_REPL_KCC_DSA_FAILURES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_neighborsw">DS_REPL_NEIGHBORS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data">DS_REPL_OBJ_META_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2">DS_REPL_OBJ_META_DATA_2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_pending_opsw">DS_REPL_PENDING_OPS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
 

 

