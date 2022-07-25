---
UID: NE:clusapi.CLUSTER_NODE_STATUS
title: CLUSTER_NODE_STATUS (clusapi.h)
description: Describes the status of a cluster node.
helpviewer_keywords: ["CLUSTER_NODE_STATUS","CLUSTER_NODE_STATUS enumeration [Failover Cluster]","NodeStatusDrainCompleted","NodeStatusDrainFailed","NodeStatusDrainInProgress","NodeStatusIsolated","NodeStatusMax","NodeStatusNormal","NodeStatusQuarantined","clusapi/CLUSTER_NODE_STATUS","clusapi/NodeStatusDrainCompleted","clusapi/NodeStatusDrainFailed","clusapi/NodeStatusDrainInProgress","clusapi/NodeStatusIsolated","clusapi/NodeStatusMax","clusapi/NodeStatusNormal","clusapi/NodeStatusQuarantined","msclus/CLUSTER_NODE_STATUS","msclus/NodeStatusDrainCompleted","msclus/NodeStatusDrainFailed","msclus/NodeStatusDrainInProgress","msclus/NodeStatusIsolated","msclus/NodeStatusMax","msclus/NodeStatusNormal","msclus/NodeStatusQuarantined","mscs.cluster_node_status"]
old-location: mscs\cluster_node_status.htm
tech.root: MsCS
ms.assetid: DFCCAB22-EF79-4E4D-959A-FE2090E4EA02
ms.date: 12/05/2018
ms.keywords: CLUSTER_NODE_STATUS, CLUSTER_NODE_STATUS enumeration [Failover Cluster], NodeStatusDrainCompleted, NodeStatusDrainFailed, NodeStatusDrainInProgress, NodeStatusIsolated, NodeStatusMax, NodeStatusNormal, NodeStatusQuarantined, clusapi/CLUSTER_NODE_STATUS, clusapi/NodeStatusDrainCompleted, clusapi/NodeStatusDrainFailed, clusapi/NodeStatusDrainInProgress, clusapi/NodeStatusIsolated, clusapi/NodeStatusMax, clusapi/NodeStatusNormal, clusapi/NodeStatusQuarantined, msclus/CLUSTER_NODE_STATUS, msclus/NodeStatusDrainCompleted, msclus/NodeStatusDrainFailed, msclus/NodeStatusDrainInProgress, msclus/NodeStatusIsolated, msclus/NodeStatusMax, msclus/NodeStatusNormal, msclus/NodeStatusQuarantined, mscs.cluster_node_status
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
req.typenames: CLUSTER_NODE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_NODE_STATUS
 - clusapi/CLUSTER_NODE_STATUS
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
 - CLUSTER_NODE_STATUS
---

# CLUSTER_NODE_STATUS enumeration


## -description

Describes the status of a cluster node. This enumeration is used by the <b>CLUSREG_NAME_NODE_STATUS_INFO</b> property.

## -enum-fields

### -field NodeStatusNormal:0x0

The node status is normal.

### -field NodeStatusIsolated:0x1

The node has been isolated.

### -field NodeStatusQuarantined:0x2

The node has been quarantined.

### -field NodeStatusDrainInProgress:0x4

The node is in the process of being drained.

### -field NodeStatusDrainCompleted:0x8

The node has completed a node drain operation.

### -field NodeStatusDrainFailed:0x10

A node drain operation failed on the node.

### -field NodeStatusAvoidPlacement:0x20

### -field NodeStatusMax

The node has experienced a node drain failure, and is therefore isolated and quarantined.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
