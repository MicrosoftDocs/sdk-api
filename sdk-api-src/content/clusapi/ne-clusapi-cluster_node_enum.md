---
UID: NE:clusapi.CLUSTER_NODE_ENUM
title: CLUSTER_NODE_ENUM
author: windows-sdk-content
description: Describes the types of cluster objects that are enumerated by the ClusterNodeEnum and ClusterNodeOpenEnum functions.
old-location: mscs\cluster_node_enum.htm
tech.root: mscs
ms.assetid: e8660f86-f4e5-4aa3-851a-94f0a230e12d
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CLUSTER_NODE_ENUM, CLUSTER_NODE_ENUM enumeration [Failover Cluster], CLUSTER_NODE_ENUM_ALL, CLUSTER_NODE_ENUM_GROUPS, CLUSTER_NODE_ENUM_NETINTERFACES, CLUSTER_NODE_ENUM_PREFERRED_GROUPS, _CLUSTER_NODE_ENUM, _CLUSTER_NODE_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_NODE_ENUM, clusapi/CLUSTER_NODE_ENUM_ALL, clusapi/CLUSTER_NODE_ENUM_GROUPS, clusapi/CLUSTER_NODE_ENUM_NETINTERFACES, clusapi/CLUSTER_NODE_ENUM_PREFERRED_GROUPS, clusapi/_CLUSTER_NODE_ENUM, msclus/CLUSTER_NODE_ENUM, msclus/CLUSTER_NODE_ENUM_ALL, msclus/CLUSTER_NODE_ENUM_GROUPS, msclus/CLUSTER_NODE_ENUM_NETINTERFACES, msclus/CLUSTER_NODE_ENUM_PREFERRED_GROUPS, msclus/_CLUSTER_NODE_ENUM, mscs.cluster_node_enum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: CLUSTER_NODE_ENUM
req.redist: 
---

# CLUSTER_NODE_ENUM enumeration


## -description


Describes the types of cluster objects that are enumerated by the 
    <a href="https://msdn.microsoft.com/e184ef8e-9ec6-4d84-a3d0-850298262b81">ClusterNodeEnum</a> and 
    <a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a> functions.


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




<a href="https://msdn.microsoft.com/e184ef8e-9ec6-4d84-a3d0-850298262b81">ClusterNodeEnum</a>



<a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

