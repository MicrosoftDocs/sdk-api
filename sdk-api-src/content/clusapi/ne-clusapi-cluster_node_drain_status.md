---
UID: NE:clusapi.CLUSTER_NODE_DRAIN_STATUS
title: CLUSTER_NODE_DRAIN_STATUS (clusapi.h)
description: Enumerates the possible values of the status of a node drain.
helpviewer_keywords: ["CLUSTER_NODE_DRAIN_STATUS","CLUSTER_NODE_DRAIN_STATUS enumeration [Failover Cluster]","ClusterNodeDrainStatusCount","NodeDrainStatusCompleted","NodeDrainStatusFailed","NodeDrainStatusInProgress","NodeDrainStatusNotInitiated","clusapi/CLUSTER_NODE_DRAIN_STATUS","clusapi/ClusterNodeDrainStatusCount","clusapi/NodeDrainStatusCompleted","clusapi/NodeDrainStatusFailed","clusapi/NodeDrainStatusInProgress","clusapi/NodeDrainStatusNotInitiated","msclus/CLUSTER_NODE_DRAIN_STATUS","msclus/ClusterNodeDrainStatusCount","msclus/NodeDrainStatusCompleted","msclus/NodeDrainStatusFailed","msclus/NodeDrainStatusInProgress","msclus/NodeDrainStatusNotInitiated","mscs.cluster_node_drain_status"]
old-location: mscs\cluster_node_drain_status.htm
tech.root: MsCS
ms.assetid: B6BC00A8-7D1E-4A86-8756-42917160DF30
ms.date: 12/05/2018
ms.keywords: CLUSTER_NODE_DRAIN_STATUS, CLUSTER_NODE_DRAIN_STATUS enumeration [Failover Cluster], ClusterNodeDrainStatusCount, NodeDrainStatusCompleted, NodeDrainStatusFailed, NodeDrainStatusInProgress, NodeDrainStatusNotInitiated, clusapi/CLUSTER_NODE_DRAIN_STATUS, clusapi/ClusterNodeDrainStatusCount, clusapi/NodeDrainStatusCompleted, clusapi/NodeDrainStatusFailed, clusapi/NodeDrainStatusInProgress, clusapi/NodeDrainStatusNotInitiated, msclus/CLUSTER_NODE_DRAIN_STATUS, msclus/ClusterNodeDrainStatusCount, msclus/NodeDrainStatusCompleted, msclus/NodeDrainStatusFailed, msclus/NodeDrainStatusInProgress, msclus/NodeDrainStatusNotInitiated, mscs.cluster_node_drain_status
f1_keywords:
- clusapi/CLUSTER_NODE_DRAIN_STATUS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ClusApi.h
- MSClus.h
api_name:
- CLUSTER_NODE_DRAIN_STATUS
targetos: Windows
req.typenames: CLUSTER_NODE_DRAIN_STATUS
req.redist: 
ms.custom: 19H1
---

# CLUSTER_NODE_DRAIN_STATUS enumeration


## -description


Enumerates the possible values of the status of a node drain. This enumeration is used in the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes-nodedrainstatus">NodeDrainStatus</a> property.


## -enum-fields




### -field NodeDrainStatusNotInitiated

Indicates that node draining has not started.


### -field NodeDrainStatusInProgress

Indicates that node draining is in progress.


### -field NodeDrainStatusCompleted

Indicates that node draining has been completed.


### -field NodeDrainStatusFailed

Indicates that node draining has failed.


### -field ClusterNodeDrainStatusCount

Defines the maximum number of drain statuses.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes-nodedrainstatus">NodeDrainStatus</a>
 

 

