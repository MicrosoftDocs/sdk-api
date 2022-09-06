---
UID: NE:msclus.CLUSTER_NODE_ENUM
title: CLUSTER_NODE_ENUM (msclus.h)
description: Describes the types of cluster objects that are enumerated by the ClusterNodeEnum and ClusterNodeOpenEnum functions.
helpviewer_keywords: ["CLUSTER_NODE_ENUM","CLUSTER_NODE_ENUM enumeration [Failover Cluster]","CLUSTER_NODE_ENUM_ALL","CLUSTER_NODE_ENUM_GROUPS","CLUSTER_NODE_ENUM_NETINTERFACES","CLUSTER_NODE_ENUM_PREFERRED_GROUPS","_CLUSTER_NODE_ENUM","_CLUSTER_NODE_ENUM enumeration [Failover Cluster]","clusapi/CLUSTER_NODE_ENUM","clusapi/CLUSTER_NODE_ENUM_ALL","clusapi/CLUSTER_NODE_ENUM_GROUPS","clusapi/CLUSTER_NODE_ENUM_NETINTERFACES","clusapi/CLUSTER_NODE_ENUM_PREFERRED_GROUPS","clusapi/_CLUSTER_NODE_ENUM","msclus/CLUSTER_NODE_ENUM","msclus/CLUSTER_NODE_ENUM_ALL","msclus/CLUSTER_NODE_ENUM_GROUPS","msclus/CLUSTER_NODE_ENUM_NETINTERFACES","msclus/CLUSTER_NODE_ENUM_PREFERRED_GROUPS","msclus/_CLUSTER_NODE_ENUM","mscs.cluster_node_enum"]
old-location: mscs\cluster_node_enum.htm
tech.root: MsCS
ms.assetid: e8660f86-f4e5-4aa3-851a-94f0a230e12d
ms.date: 12/05/2018
ms.keywords: CLUSTER_NODE_ENUM, CLUSTER_NODE_ENUM enumeration [Failover Cluster], CLUSTER_NODE_ENUM_ALL, CLUSTER_NODE_ENUM_GROUPS, CLUSTER_NODE_ENUM_NETINTERFACES, CLUSTER_NODE_ENUM_PREFERRED_GROUPS, _CLUSTER_NODE_ENUM, _CLUSTER_NODE_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_NODE_ENUM, clusapi/CLUSTER_NODE_ENUM_ALL, clusapi/CLUSTER_NODE_ENUM_GROUPS, clusapi/CLUSTER_NODE_ENUM_NETINTERFACES, clusapi/CLUSTER_NODE_ENUM_PREFERRED_GROUPS, clusapi/_CLUSTER_NODE_ENUM, msclus/CLUSTER_NODE_ENUM, msclus/CLUSTER_NODE_ENUM_ALL, msclus/CLUSTER_NODE_ENUM_GROUPS, msclus/CLUSTER_NODE_ENUM_NETINTERFACES, msclus/CLUSTER_NODE_ENUM_PREFERRED_GROUPS, msclus/_CLUSTER_NODE_ENUM, mscs.cluster_node_enum
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
req.typenames: CLUSTER_NODE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_NODE_ENUM
 - msclus/CLUSTER_NODE_ENUM
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
 - CLUSTER_NODE_ENUM
---

# CLUSTER_NODE_ENUM enumeration


## -description

Describes the types of cluster objects that are enumerated by the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeenum">ClusterNodeEnum</a> and 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a> functions.

## -enum-fields

### -field CLUSTER_NODE_ENUM_NETINTERFACES:0x1

Network interfaces on the node.

### -field CLUSTER_NODE_ENUM_GROUPS:0x2

Cluster groups on the node.

<b>Windows Server 2008:  </b>This value is not supported before 
        Windows Server 2008 R2.

### -field CLUSTER_NODE_ENUM_PREFERRED_GROUPS:0x4

Cluster groups that list this node as their preferred owner.

<b>Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is supported before 
        Windows Server 2012 R2.

### -field CLUSTER_NODE_ENUM_ALL

Network interfaces on the node, groups on the node, and groups that list the node as their preferred owner..

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeenum">ClusterNodeEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
