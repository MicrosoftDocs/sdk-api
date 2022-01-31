---
UID: NE:msclus.CLUSTER_NODE_STATE
title: CLUSTER_NODE_STATE (msclus.h)
description: Describes the state of a cluster node.
helpviewer_keywords: ["CLUSTER_NODE_STATE","CLUSTER_NODE_STATE enumeration [Failover Cluster]","ClusterNodeDown","ClusterNodeJoining","ClusterNodePaused","ClusterNodeStateUnknown","ClusterNodeUp","_CLUSTER_NODE_STATE","_CLUSTER_NODE_STATE enumeration [Failover Cluster]","clusapi/CLUSTER_NODE_STATE","clusapi/ClusterNodeDown","clusapi/ClusterNodeJoining","clusapi/ClusterNodePaused","clusapi/ClusterNodeStateUnknown","clusapi/ClusterNodeUp","clusapi/_CLUSTER_NODE_STATE","msclus/CLUSTER_NODE_STATE","msclus/ClusterNodeDown","msclus/ClusterNodeJoining","msclus/ClusterNodePaused","msclus/ClusterNodeStateUnknown","msclus/ClusterNodeUp","msclus/_CLUSTER_NODE_STATE","mscs.cluster_node_state"]
old-location: mscs\cluster_node_state.htm
tech.root: MsCS
ms.assetid: 25bc275e-8d9c-43b3-8f95-dd3fd2cbe3ce
ms.date: 12/05/2018
ms.keywords: CLUSTER_NODE_STATE, CLUSTER_NODE_STATE enumeration [Failover Cluster], ClusterNodeDown, ClusterNodeJoining, ClusterNodePaused, ClusterNodeStateUnknown, ClusterNodeUp, _CLUSTER_NODE_STATE, _CLUSTER_NODE_STATE enumeration [Failover Cluster], clusapi/CLUSTER_NODE_STATE, clusapi/ClusterNodeDown, clusapi/ClusterNodeJoining, clusapi/ClusterNodePaused, clusapi/ClusterNodeStateUnknown, clusapi/ClusterNodeUp, clusapi/_CLUSTER_NODE_STATE, msclus/CLUSTER_NODE_STATE, msclus/ClusterNodeDown, msclus/ClusterNodeJoining, msclus/ClusterNodePaused, msclus/ClusterNodeStateUnknown, msclus/ClusterNodeUp, msclus/_CLUSTER_NODE_STATE, mscs.cluster_node_state
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
req.typenames: CLUSTER_NODE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_NODE_STATE
 - msclus/CLUSTER_NODE_STATE
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
 - CLUSTER_NODE_STATE
---

# CLUSTER_NODE_STATE enumeration


## -description

Describes the state of a cluster node. The 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternodestate">GetClusterNodeState</a> and 
    <a href="/previous-versions/windows/desktop/mscs/clusnode-state">State</a> properties use this enumeration.

## -enum-fields

### -field ClusterNodeStateUnknown:-1

The operation was not successful. For more information about the error, call the function 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

### -field ClusterNodeUp

The node is physically plugged in, turned on, booted, and capable of executing programs. This value is also 
       used by the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-setclusterserviceaccountpassword">SetClusterServiceAccountPassword</a> 
       function and <a href="/previous-versions/windows/desktop/mscs/clusnode-resume">Resume</a> method.

### -field ClusterNodeDown

The node is turned off or not operational.

### -field ClusterNodePaused

The node is running but not participating in cluster operations. This value is also used by the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-pauseclusternode">PauseClusterNode</a> and 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-setclusterserviceaccountpassword">SetClusterServiceAccountPassword</a> 
       functions. This value is also used <a href="/previous-versions/windows/desktop/mscs/clusnode-pause">Pause</a> method.

### -field ClusterNodeJoining

The node is in the process of joining a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternodestate">GetClusterNodeState</a>



<a href="/previous-versions/windows/desktop/mscs/clusnode-pause">Pause Method of the ClusNode Object</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-pauseclusternode">PauseClusterNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-setclusterserviceaccountpassword">SetClusterServiceAccountPassword</a>



<a href="/previous-versions/windows/desktop/mscs/clusnode-state">State Property of the ClusNode Object</a>
