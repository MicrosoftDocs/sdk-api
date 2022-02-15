---
UID: NE:msclus.CLUSTER_RESOURCE_TYPE_ENUM
title: CLUSTER_RESOURCE_TYPE_ENUM (msclus.h)
description: Describes the type of cluster object being enumerated by the ClusterResourceTypeEnum and ClusterResourceTypeOpenEnum functions.
helpviewer_keywords: ["CLUSTER_RESOURCE_TYPE_ENUM","CLUSTER_RESOURCE_TYPE_ENUM enumeration [Failover Cluster]","CLUSTER_RESOURCE_TYPE_ENUM_ALL","CLUSTER_RESOURCE_TYPE_ENUM_NODES","CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES","_CLUSTER_RESOURCE_TYPE_ENUM","_CLUSTER_RESOURCE_TYPE_ENUM enumeration [Failover Cluster]","clusapi/CLUSTER_RESOURCE_TYPE_ENUM","clusapi/CLUSTER_RESOURCE_TYPE_ENUM_ALL","clusapi/CLUSTER_RESOURCE_TYPE_ENUM_NODES","clusapi/CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES","clusapi/_CLUSTER_RESOURCE_TYPE_ENUM","msclus/CLUSTER_RESOURCE_TYPE_ENUM","msclus/CLUSTER_RESOURCE_TYPE_ENUM_ALL","msclus/CLUSTER_RESOURCE_TYPE_ENUM_NODES","msclus/CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES","msclus/_CLUSTER_RESOURCE_TYPE_ENUM","mscs.cluster_resource_type_enum"]
old-location: mscs\cluster_resource_type_enum.htm
tech.root: MsCS
ms.assetid: f8356cb3-303c-4294-a634-d91d5141004a
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_TYPE_ENUM, CLUSTER_RESOURCE_TYPE_ENUM enumeration [Failover Cluster], CLUSTER_RESOURCE_TYPE_ENUM_ALL, CLUSTER_RESOURCE_TYPE_ENUM_NODES, CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, _CLUSTER_RESOURCE_TYPE_ENUM, _CLUSTER_RESOURCE_TYPE_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_TYPE_ENUM, clusapi/CLUSTER_RESOURCE_TYPE_ENUM_ALL, clusapi/CLUSTER_RESOURCE_TYPE_ENUM_NODES, clusapi/CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, clusapi/_CLUSTER_RESOURCE_TYPE_ENUM, msclus/CLUSTER_RESOURCE_TYPE_ENUM, msclus/CLUSTER_RESOURCE_TYPE_ENUM_ALL, msclus/CLUSTER_RESOURCE_TYPE_ENUM_NODES, msclus/CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, msclus/_CLUSTER_RESOURCE_TYPE_ENUM, mscs.cluster_resource_type_enum
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
req.typenames: CLUSTER_RESOURCE_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_RESOURCE_TYPE_ENUM
 - msclus/CLUSTER_RESOURCE_TYPE_ENUM
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
 - CLUSTER_RESOURCE_TYPE_ENUM
---

# CLUSTER_RESOURCE_TYPE_ENUM enumeration


## -description

Describes the type of cluster object being enumerated by the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeenum">ClusterResourceTypeEnum</a> and 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeopenenum">ClusterResourceTypeOpenEnum</a> 
    functions.

## -enum-fields

### -field CLUSTER_RESOURCE_TYPE_ENUM_NODES:0x1

The object is a node that can be a possible owner of the resource type.

### -field CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES:0x2

The object is a resource that is an instance of the resource type.

<b>Windows Server 2008:  </b>This value is not supported before Windows Server 2008 R2. To emulate this on earlier platforms, 
       enumerate all resources in the cluster (see the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenum">ClusterOpenEnum</a> function) and filter the results 
       using the <a href="/windows/desktop/api/resapi/nf-resapi-resutilresourcetypesequal">ResUtilResourceTypesEqual</a> 
       function. If the call is made on a system without ResUtils.dll, then use the steps mentioned in the Remarks 
       section of the <b>ResUtilResourceTypesEqual</b> 
       function.

### -field CLUSTER_RESOURCE_TYPE_ENUM_ALL

All cluster objects identified by the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeenum">ClusterResourceTypeEnum</a> and 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeopenenum">ClusterResourceTypeOpenEnum</a> 
       functions.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeenum">ClusterResourceTypeEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeopenenum">ClusterResourceTypeOpenEnum</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
