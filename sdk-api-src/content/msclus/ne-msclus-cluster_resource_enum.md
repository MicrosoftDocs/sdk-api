---
UID: NE:msclus.CLUSTER_RESOURCE_ENUM
title: CLUSTER_RESOURCE_ENUM (msclus.h)
description: Describes the type of cluster object being enumerated by the ClusterResourceEnum or ClusterResourceOpenEnum functions.
helpviewer_keywords: ["CLUSTER_RESOURCE_ENUM","CLUSTER_RESOURCE_ENUM enumeration [Failover Cluster]","CLUSTER_RESOURCE_ENUM_ALL","CLUSTER_RESOURCE_ENUM_DEPENDS","CLUSTER_RESOURCE_ENUM_NODES","CLUSTER_RESOURCE_ENUM_PROVIDES","_CLUSTER_RESOURCE_ENUM","_CLUSTER_RESOURCE_ENUM enumeration [Failover Cluster]","clusapi/CLUSTER_RESOURCE_ENUM","clusapi/CLUSTER_RESOURCE_ENUM_ALL","clusapi/CLUSTER_RESOURCE_ENUM_DEPENDS","clusapi/CLUSTER_RESOURCE_ENUM_NODES","clusapi/CLUSTER_RESOURCE_ENUM_PROVIDES","clusapi/_CLUSTER_RESOURCE_ENUM","msclus/CLUSTER_RESOURCE_ENUM","msclus/CLUSTER_RESOURCE_ENUM_ALL","msclus/CLUSTER_RESOURCE_ENUM_DEPENDS","msclus/CLUSTER_RESOURCE_ENUM_NODES","msclus/CLUSTER_RESOURCE_ENUM_PROVIDES","msclus/_CLUSTER_RESOURCE_ENUM","mscs.cluster_resource_enum"]
old-location: mscs\cluster_resource_enum.htm
tech.root: MsCS
ms.assetid: 8b59ab43-7e03-4ddf-82cc-9945e9da6462
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_ENUM, CLUSTER_RESOURCE_ENUM enumeration [Failover Cluster], CLUSTER_RESOURCE_ENUM_ALL, CLUSTER_RESOURCE_ENUM_DEPENDS, CLUSTER_RESOURCE_ENUM_NODES, CLUSTER_RESOURCE_ENUM_PROVIDES, _CLUSTER_RESOURCE_ENUM, _CLUSTER_RESOURCE_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_ENUM, clusapi/CLUSTER_RESOURCE_ENUM_ALL, clusapi/CLUSTER_RESOURCE_ENUM_DEPENDS, clusapi/CLUSTER_RESOURCE_ENUM_NODES, clusapi/CLUSTER_RESOURCE_ENUM_PROVIDES, clusapi/_CLUSTER_RESOURCE_ENUM, msclus/CLUSTER_RESOURCE_ENUM, msclus/CLUSTER_RESOURCE_ENUM_ALL, msclus/CLUSTER_RESOURCE_ENUM_DEPENDS, msclus/CLUSTER_RESOURCE_ENUM_NODES, msclus/CLUSTER_RESOURCE_ENUM_PROVIDES, msclus/_CLUSTER_RESOURCE_ENUM, mscs.cluster_resource_enum
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: CLUSTER_RESOURCE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_RESOURCE_ENUM
 - msclus/CLUSTER_RESOURCE_ENUM
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
 - CLUSTER_RESOURCE_ENUM
---

# CLUSTER_RESOURCE_ENUM enumeration


## -description

Describes the type of cluster object being enumerated by the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a> or 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a> 
    functions.

## -enum-fields

### -field CLUSTER_RESOURCE_ENUM_DEPENDS:0x1

A resource that the resource identified by the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a> or 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a> functions directly 
       depends on.

### -field CLUSTER_RESOURCE_ENUM_PROVIDES:0x2

A resource that directly depends on the resource identified by the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a> or 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a> functions.

### -field CLUSTER_RESOURCE_ENUM_NODES:0x4

A node that can host the resource identified by the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a> or 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a> functions.

### -field CLUSTER_RESOURCE_ENUM_ALL

All nodes and resources identified by the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a> or 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a> functions.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
