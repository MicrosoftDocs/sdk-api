---
UID: NE:clusapi.CLUSTER_GROUP_ENUM
title: CLUSTER_GROUP_ENUM (clusapi.h)
description: Describes the type of cluster object being enumerated by the ClusterGroupEnum and ClusterGroupOpenEnum functions.
helpviewer_keywords: ["CLUSTER_GROUP_ENUM","CLUSTER_GROUP_ENUM enumeration [Failover Cluster]","CLUSTER_GROUP_ENUM_ALL","CLUSTER_GROUP_ENUM_CONTAINS","CLUSTER_GROUP_ENUM_NODES","_CLUSTER_GROUP_ENUM","_CLUSTER_GROUP_ENUM enumeration [Failover Cluster]","clusapi/CLUSTER_GROUP_ENUM","clusapi/CLUSTER_GROUP_ENUM_ALL","clusapi/CLUSTER_GROUP_ENUM_CONTAINS","clusapi/CLUSTER_GROUP_ENUM_NODES","clusapi/_CLUSTER_GROUP_ENUM","msclus/CLUSTER_GROUP_ENUM","msclus/CLUSTER_GROUP_ENUM_ALL","msclus/CLUSTER_GROUP_ENUM_CONTAINS","msclus/CLUSTER_GROUP_ENUM_NODES","msclus/_CLUSTER_GROUP_ENUM","mscs.cluster_group_enum"]
old-location: mscs\cluster_group_enum.htm
tech.root: MsCS
ms.assetid: c70bc230-850b-4290-8275-f60ffc8d66bd
ms.date: 12/05/2018
ms.keywords: CLUSTER_GROUP_ENUM, CLUSTER_GROUP_ENUM enumeration [Failover Cluster], CLUSTER_GROUP_ENUM_ALL, CLUSTER_GROUP_ENUM_CONTAINS, CLUSTER_GROUP_ENUM_NODES, _CLUSTER_GROUP_ENUM, _CLUSTER_GROUP_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_GROUP_ENUM, clusapi/CLUSTER_GROUP_ENUM_ALL, clusapi/CLUSTER_GROUP_ENUM_CONTAINS, clusapi/CLUSTER_GROUP_ENUM_NODES, clusapi/_CLUSTER_GROUP_ENUM, msclus/CLUSTER_GROUP_ENUM, msclus/CLUSTER_GROUP_ENUM_ALL, msclus/CLUSTER_GROUP_ENUM_CONTAINS, msclus/CLUSTER_GROUP_ENUM_NODES, msclus/_CLUSTER_GROUP_ENUM, mscs.cluster_group_enum
req.header: clusapi.h
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
req.typenames: CLUSTER_GROUP_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_GROUP_ENUM
 - clusapi/CLUSTER_GROUP_ENUM
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
 - CLUSTER_GROUP_ENUM
---

# CLUSTER_GROUP_ENUM enumeration


## -description

Describes the type of cluster object being enumerated by the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupenum">ClusterGroupEnum</a> and 
    <a href="/windows/win32/api/clusapi/nf-clusapi-clustergroupopenenum">ClusterGroupOpenEnum</a> functions.

## -enum-fields

### -field CLUSTER_GROUP_ENUM_CONTAINS:0x00000001

The resources in the group.

### -field CLUSTER_GROUP_ENUM_NODES:0x00000002

The nodes in the preferred owners list of the group.

### -field CLUSTER_GROUP_ENUM_ALL

All the resources in the group and all the nodes in the preferred owners list of the group.

## -remarks

The <b>CLUSTER_GROUP_ENUM_ALL</b> enumeration value is not a valid value for the 
     <i>lpdwType</i> parameter of the 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupenum">ClusterGroupEnum</a> function.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupenum">ClusterGroupEnum</a>



<a href="/windows/win32/api/clusapi/nf-clusapi-clustergroupopenenum">ClusterGroupOpenEnum</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
