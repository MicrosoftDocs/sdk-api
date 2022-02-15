---
UID: NE:msclus.CLUSTER_CHANGE_NODE_V2
title: CLUSTER_CHANGE_NODE_V2 (msclus.h)
description: Defines the notifications that are generated for a cluster node.
helpviewer_keywords: ["CLUSTER_CHANGE_NODE_ALL_V2","CLUSTER_CHANGE_NODE_COMMON_PROPERTY_V2","CLUSTER_CHANGE_NODE_DELETED_V2","CLUSTER_CHANGE_NODE_GROUP_GAINED_V2","CLUSTER_CHANGE_NODE_GROUP_LOST_V2","CLUSTER_CHANGE_NODE_HANDLE_CLOSE_V2","CLUSTER_CHANGE_NODE_NETINTERFACE_ADDED_V2","CLUSTER_CHANGE_NODE_PRIVATE_PROPERTY_V2","CLUSTER_CHANGE_NODE_STATE_V2","CLUSTER_CHANGE_NODE_V2","CLUSTER_CHANGE_NODE_V2 enumeration [Failover Cluster]","clusapi/CLUSTER_CHANGE_NODE_ALL_V2","clusapi/CLUSTER_CHANGE_NODE_COMMON_PROPERTY_V2","clusapi/CLUSTER_CHANGE_NODE_DELETED_V2","clusapi/CLUSTER_CHANGE_NODE_GROUP_GAINED_V2","clusapi/CLUSTER_CHANGE_NODE_GROUP_LOST_V2","clusapi/CLUSTER_CHANGE_NODE_HANDLE_CLOSE_V2","clusapi/CLUSTER_CHANGE_NODE_NETINTERFACE_ADDED_V2","clusapi/CLUSTER_CHANGE_NODE_PRIVATE_PROPERTY_V2","clusapi/CLUSTER_CHANGE_NODE_STATE_V2","clusapi/CLUSTER_CHANGE_NODE_V2","msclus/CLUSTER_CHANGE_NODE_ALL_V2","msclus/CLUSTER_CHANGE_NODE_COMMON_PROPERTY_V2","msclus/CLUSTER_CHANGE_NODE_DELETED_V2","msclus/CLUSTER_CHANGE_NODE_GROUP_GAINED_V2","msclus/CLUSTER_CHANGE_NODE_GROUP_LOST_V2","msclus/CLUSTER_CHANGE_NODE_HANDLE_CLOSE_V2","msclus/CLUSTER_CHANGE_NODE_NETINTERFACE_ADDED_V2","msclus/CLUSTER_CHANGE_NODE_PRIVATE_PROPERTY_V2","msclus/CLUSTER_CHANGE_NODE_STATE_V2","msclus/CLUSTER_CHANGE_NODE_V2","mscs.cluster_change_node_v2"]
old-location: mscs\cluster_change_node_v2.htm
tech.root: MsCS
ms.assetid: E51A9C6C-D874-44CE-B190-60E44F6B92B2
ms.date: 12/05/2018
ms.keywords: CLUSTER_CHANGE_NODE_ALL_V2, CLUSTER_CHANGE_NODE_COMMON_PROPERTY_V2, CLUSTER_CHANGE_NODE_DELETED_V2, CLUSTER_CHANGE_NODE_GROUP_GAINED_V2, CLUSTER_CHANGE_NODE_GROUP_LOST_V2, CLUSTER_CHANGE_NODE_HANDLE_CLOSE_V2, CLUSTER_CHANGE_NODE_NETINTERFACE_ADDED_V2, CLUSTER_CHANGE_NODE_PRIVATE_PROPERTY_V2, CLUSTER_CHANGE_NODE_STATE_V2, CLUSTER_CHANGE_NODE_V2, CLUSTER_CHANGE_NODE_V2 enumeration [Failover Cluster], clusapi/CLUSTER_CHANGE_NODE_ALL_V2, clusapi/CLUSTER_CHANGE_NODE_COMMON_PROPERTY_V2, clusapi/CLUSTER_CHANGE_NODE_DELETED_V2, clusapi/CLUSTER_CHANGE_NODE_GROUP_GAINED_V2, clusapi/CLUSTER_CHANGE_NODE_GROUP_LOST_V2, clusapi/CLUSTER_CHANGE_NODE_HANDLE_CLOSE_V2, clusapi/CLUSTER_CHANGE_NODE_NETINTERFACE_ADDED_V2, clusapi/CLUSTER_CHANGE_NODE_PRIVATE_PROPERTY_V2, clusapi/CLUSTER_CHANGE_NODE_STATE_V2, clusapi/CLUSTER_CHANGE_NODE_V2, msclus/CLUSTER_CHANGE_NODE_ALL_V2, msclus/CLUSTER_CHANGE_NODE_COMMON_PROPERTY_V2, msclus/CLUSTER_CHANGE_NODE_DELETED_V2, msclus/CLUSTER_CHANGE_NODE_GROUP_GAINED_V2, msclus/CLUSTER_CHANGE_NODE_GROUP_LOST_V2, msclus/CLUSTER_CHANGE_NODE_HANDLE_CLOSE_V2, msclus/CLUSTER_CHANGE_NODE_NETINTERFACE_ADDED_V2, msclus/CLUSTER_CHANGE_NODE_PRIVATE_PROPERTY_V2, msclus/CLUSTER_CHANGE_NODE_STATE_V2, msclus/CLUSTER_CHANGE_NODE_V2, mscs.cluster_change_node_v2
req.header: msclus.h
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
req.typenames: CLUSTER_CHANGE_NODE_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_CHANGE_NODE_V2
 - msclus/CLUSTER_CHANGE_NODE_V2
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
 - CLUSTER_CHANGE_NODE_V2
---

# CLUSTER_CHANGE_NODE_V2 enumeration


## -description

Defines the notifications that are generated for a cluster node.

## -enum-fields

### -field CLUSTER_CHANGE_NODE_NETINTERFACE_ADDED_V2:0x1

Indicates that the network interface for the cluster node has been added.

### -field CLUSTER_CHANGE_NODE_DELETED_V2:0x2

Indicates that the cluster node has been deleted.

### -field CLUSTER_CHANGE_NODE_COMMON_PROPERTY_V2:0x4

Indicates that the common properties for the cluster node have been changed.

### -field CLUSTER_CHANGE_NODE_PRIVATE_PROPERTY_V2:0x8

Indicates that the private properties for the cluster node have been changed.

### -field CLUSTER_CHANGE_NODE_STATE_V2:0x10

Indicates that the state of the cluster node has changed.

### -field CLUSTER_CHANGE_NODE_GROUP_GAINED_V2:0x20

Indicates that the cluster node has gained a group.

### -field CLUSTER_CHANGE_NODE_GROUP_LOST_V2:0x40

Indicates that the cluster node has lost a group.

### -field CLUSTER_CHANGE_NODE_HANDLE_CLOSE_V2:0x80

Indicates that the cluster node's context handle was closed.

### -field CLUSTER_CHANGE_NODE_ALL_V2

Indicates all V2 cluster node notifications.

## -remarks

Protocol version 2.0 servers do not support this enumeration.

