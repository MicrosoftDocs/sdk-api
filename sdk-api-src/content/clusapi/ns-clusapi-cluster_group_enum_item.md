---
UID: NS:clusapi._CLUSTER_GROUP_ENUM_ITEM
title: CLUSTER_GROUP_ENUM_ITEM (clusapi.h)
description: CLUSTER_GROUP_ENUM_ITEM (clusapi.h) contains the properties of a cluster group and is used to enumerate cluster groups in the ClusterGroupEnumEx function.
helpviewer_keywords: ["*PCLUSTER_GROUP_ENUM_ITEM","CLUSTER_GROUP_ENUM_ITEM","CLUSTER_GROUP_ENUM_ITEM structure [Failover Cluster]","PCLUSTER_GROUP_ENUM_ITEM","PCLUSTER_GROUP_ENUM_ITEM structure pointer [Failover Cluster]","_CLUSTER_GROUP_ENUM_ITEM","_CLUSTER_GROUP_ENUM_ITEM structure [Failover Cluster]","clusapi/CLUSTER_GROUP_ENUM_ITEM","clusapi/PCLUSTER_GROUP_ENUM_ITEM","clusapi/_CLUSTER_GROUP_ENUM_ITEM","msclus/CLUSTER_GROUP_ENUM_ITEM","msclus/PCLUSTER_GROUP_ENUM_ITEM","msclus/_CLUSTER_GROUP_ENUM_ITEM","mscs.cluster_group_enum_item"]
old-location: mscs\cluster_group_enum_item.htm
tech.root: MsCS
ms.assetid: B6436F83-2A10-4E93-8141-9BCFF744E41B
ms.date: 08/03/2022
ms.keywords: '*PCLUSTER_GROUP_ENUM_ITEM, CLUSTER_GROUP_ENUM_ITEM, CLUSTER_GROUP_ENUM_ITEM structure [Failover Cluster], PCLUSTER_GROUP_ENUM_ITEM, PCLUSTER_GROUP_ENUM_ITEM structure pointer [Failover Cluster], _CLUSTER_GROUP_ENUM_ITEM, _CLUSTER_GROUP_ENUM_ITEM structure [Failover Cluster], clusapi/CLUSTER_GROUP_ENUM_ITEM, clusapi/PCLUSTER_GROUP_ENUM_ITEM, clusapi/_CLUSTER_GROUP_ENUM_ITEM, msclus/CLUSTER_GROUP_ENUM_ITEM, msclus/PCLUSTER_GROUP_ENUM_ITEM, msclus/_CLUSTER_GROUP_ENUM_ITEM, mscs.cluster_group_enum_item'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: CLUSTER_GROUP_ENUM_ITEM, *PCLUSTER_GROUP_ENUM_ITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_GROUP_ENUM_ITEM
 - clusapi/_CLUSTER_GROUP_ENUM_ITEM
 - PCLUSTER_GROUP_ENUM_ITEM
 - clusapi/PCLUSTER_GROUP_ENUM_ITEM
 - CLUSTER_GROUP_ENUM_ITEM
 - clusapi/CLUSTER_GROUP_ENUM_ITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_GROUP_ENUM_ITEM
---

## -description

Contains the properties of a cluster group. This structure  is used to enumerate cluster groups in the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupenumex">ClusterGroupEnumEx</a> function.

## -struct-fields

### -field dwVersion

The version of the 
      <b>CLUSTER_GROUP_ENUM_ITEM</b> structure.

### -field cbId

The size, in bytes, of the <b>lpszId</b> field.

### -field lpszId

The Id of the cluster group.

### -field cbName

The size, in bytes, of the <b>IpszName</b> field.

### -field lpszName

The name of the cluster group.

### -field state

The current state of the cluster group.

### -field cbOwnerNode

The size, in bytes, of the <b>IpszOwnerNode</b> field.

### -field lpszOwnerNode

The name of the cluster node hosting the group.

### -field dwFlags

The group flags.

### -field cbProperties

The size, in bytes, of the <b>pProperties</b> field.

### -field pProperties

A pointer to a list of names of common properties.

### -field cbRoProperties

The size, in bytes, of the <b>pRoProperties</b> field.

### -field pRoProperties

A pointer to a list of names of read-only common properties.
