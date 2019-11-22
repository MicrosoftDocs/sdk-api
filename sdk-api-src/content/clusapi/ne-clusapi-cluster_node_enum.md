---
UID: NE:clusapi.CLUSTER_NODE_ENUM
title: CLUSTER_NODE_ENUM (clusapi.h)

description: Describes the types of cluster objects that are enumerated by the ClusterNodeEnum and ClusterNodeOpenEnum functions.
old-location: mscs\cluster_node_enum.htm
tech.root: MsCS
ms.assetid: e8660f86-f4e5-4aa3-851a-94f0a230e12d

ms.date: 12/05/2018
ms.keywords: CLUSTER_NODE_ENUM, CLUSTER_NODE_ENUM enumeration [Failover Cluster], CLUSTER_NODE_ENUM_ALL, CLUSTER_NODE_ENUM_GROUPS, CLUSTER_NODE_ENUM_NETINTERFACES, CLUSTER_NODE_ENUM_PREFERRED_GROUPS, _CLUSTER_NODE_ENUM, _CLUSTER_NODE_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_NODE_ENUM, clusapi/CLUSTER_NODE_ENUM_ALL, clusapi/CLUSTER_NODE_ENUM_GROUPS, clusapi/CLUSTER_NODE_ENUM_NETINTERFACES, clusapi/CLUSTER_NODE_ENUM_PREFERRED_GROUPS, clusapi/_CLUSTER_NODE_ENUM, msclus/CLUSTER_NODE_ENUM, msclus/CLUSTER_NODE_ENUM_ALL, msclus/CLUSTER_NODE_ENUM_GROUPS, msclus/CLUSTER_NODE_ENUM_NETINTERFACES, msclus/CLUSTER_NODE_ENUM_PREFERRED_GROUPS, msclus/_CLUSTER_NODE_ENUM, mscs.cluster_node_enum
ms.topic: enum
f1_keywords: 
 - "clusapi/CLUSTER_NODE_ENUM"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: CLUSTER_NODE_ENUM
req.redist: 
ms.custom: 19H1
---

# CLUSTER_NODE_ENUM enumeration


## -description


Describes the types of cluster objects that are enumerated by the 
    <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeenum">ClusterNodeEnum</a> and 
    <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a> functions.


## -enum-fields




### -field CLUSTER_NODE_ENUM_NETINTERFACES

Network interfaces on the node.


### -field CLUSTER_NODE_ENUM_GROUPS

Cluster groups on the node.

<b>Windows Server 2008:  </b>This value is not supported before 
        Windows Server 2008 R2.


### -field CLUSTER_NODE_ENUM_PREFERRED_GROUPS

Cluster groups that list this node as their preferred owner.

<b>Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is supported before 
        Windows Server 2012 R2.


### -field CLUSTER_NODE_ENUM_ALL

Network interfaces on the node, groups on the node, and groups that list the node as their preferred owner..


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeenum">ClusterNodeEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
 

 

