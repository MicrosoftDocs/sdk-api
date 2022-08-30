---
UID: NS:clusapi._CLUSTER_RESOURCE_ENUM_ITEM
title: CLUSTER_RESOURCE_ENUM_ITEM (clusapi.h)
description: CLUSTER_RESOURCE_ENUM_ITEM represents the properties of a cluster resource and is used to enumerate cluster resources in the ClusterResourceEnumEx function.
helpviewer_keywords: ["*PCLUSTER_RESOURCE_ENUM_ITEM","CLUSTER_RESOURCE_ENUM_ITEM","CLUSTER_RESOURCE_ENUM_ITEM structure [Failover Cluster]","PCLUSTER_RESOURCE_ENUM_ITEM","PCLUSTER_RESOURCE_ENUM_ITEM structure pointer [Failover Cluster]","_CLUSTER_RESOURCE_ENUM_ITEM","_CLUSTER_RESOURCE_ENUM_ITEM structure [Failover Cluster]","clusapi/CLUSTER_RESOURCE_ENUM_ITEM","clusapi/PCLUSTER_RESOURCE_ENUM_ITEM","clusapi/_CLUSTER_RESOURCE_ENUM_ITEM","msclus/CLUSTER_RESOURCE_ENUM_ITEM","msclus/PCLUSTER_RESOURCE_ENUM_ITEM","msclus/_CLUSTER_RESOURCE_ENUM_ITEM","mscs.cluster_resource_enum_item"]
old-location: mscs\cluster_resource_enum_item.htm
tech.root: MsCS
ms.assetid: B8369B29-F72A-4642-93CB-23F04E680663
ms.date: 08/03/2022
ms.keywords: '*PCLUSTER_RESOURCE_ENUM_ITEM, CLUSTER_RESOURCE_ENUM_ITEM, CLUSTER_RESOURCE_ENUM_ITEM structure [Failover Cluster], PCLUSTER_RESOURCE_ENUM_ITEM, PCLUSTER_RESOURCE_ENUM_ITEM structure pointer [Failover Cluster], _CLUSTER_RESOURCE_ENUM_ITEM, _CLUSTER_RESOURCE_ENUM_ITEM structure [Failover Cluster], clusapi/CLUSTER_RESOURCE_ENUM_ITEM, clusapi/PCLUSTER_RESOURCE_ENUM_ITEM, clusapi/_CLUSTER_RESOURCE_ENUM_ITEM, msclus/CLUSTER_RESOURCE_ENUM_ITEM, msclus/PCLUSTER_RESOURCE_ENUM_ITEM, msclus/_CLUSTER_RESOURCE_ENUM_ITEM, mscs.cluster_resource_enum_item'
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
req.typenames: CLUSTER_RESOURCE_ENUM_ITEM, *PCLUSTER_RESOURCE_ENUM_ITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_RESOURCE_ENUM_ITEM
 - clusapi/_CLUSTER_RESOURCE_ENUM_ITEM
 - PCLUSTER_RESOURCE_ENUM_ITEM
 - clusapi/PCLUSTER_RESOURCE_ENUM_ITEM
 - CLUSTER_RESOURCE_ENUM_ITEM
 - clusapi/CLUSTER_RESOURCE_ENUM_ITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MsClus.h
api_name:
 - CLUSTER_RESOURCE_ENUM_ITEM
---

## -description

Represents the properties of a cluster resource. This structure is used to enumerate cluster resources in the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenumex">ClusterResourceEnumEx</a> function.

## -struct-fields

### -field dwVersion

The version of this structure.

### -field cbId

The size, in bytes, of the <b>lpszId</b> field.

### -field lpszId

The ID of the cluster resource.

### -field cbName

The size, in bytes, of the <b>IpszName</b> field.

### -field lpszName

The name of the cluster resource.

### -field cbOwnerGroupName

The size, in bytes, of the <b>IpszOwnerNode</b> field.

### -field lpszOwnerGroupName

The name of the cluster resource that  hosts the group.

### -field cbOwnerGroupId

The size, in bytes, of the <b>lpszOwnerGroupId</b> field.

### -field lpszOwnerGroupId

The group ID of the cluster group for the resource.

### -field cbProperties

The size, in bytes, of the <b>pProperties</b> field.

### -field pProperties

A pointer to a list of names of common properties.

### -field cbRoProperties

The size, in bytes, of the <b>pRoProperties</b> field.

### -field pRoProperties

A pointer to a list of names of read-only common properties.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenumex">ClusterResourceEnumEx</a>

<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>
