---
UID: NE:clusapi.CLUSTER_NETWORK_STATE
title: CLUSTER_NETWORK_STATE (clusapi.h)
description: Enumerates the possible values of the state of a network.
helpviewer_keywords: ["CLUSTER_NETWORK_STATE","CLUSTER_NETWORK_STATE enumeration [Failover Cluster]","ClusterNetworkDown","ClusterNetworkPartitioned","ClusterNetworkStateUnknown","ClusterNetworkUnavailable","ClusterNetworkUp","_CLUSTER_NETWORK_STATE","_CLUSTER_NETWORK_STATE enumeration [Failover Cluster]","clusapi/CLUSTER_NETWORK_STATE","clusapi/ClusterNetworkDown","clusapi/ClusterNetworkPartitioned","clusapi/ClusterNetworkStateUnknown","clusapi/ClusterNetworkUnavailable","clusapi/ClusterNetworkUp","clusapi/_CLUSTER_NETWORK_STATE","msclus/CLUSTER_NETWORK_STATE","msclus/ClusterNetworkDown","msclus/ClusterNetworkPartitioned","msclus/ClusterNetworkStateUnknown","msclus/ClusterNetworkUnavailable","msclus/ClusterNetworkUp","msclus/_CLUSTER_NETWORK_STATE","mscs.cluster_network_state"]
old-location: mscs\cluster_network_state.htm
tech.root: MsCS
ms.assetid: 1a9e3ff0-eb5a-4a2e-ae19-e70213dc1a4a
ms.date: 12/05/2018
ms.keywords: CLUSTER_NETWORK_STATE, CLUSTER_NETWORK_STATE enumeration [Failover Cluster], ClusterNetworkDown, ClusterNetworkPartitioned, ClusterNetworkStateUnknown, ClusterNetworkUnavailable, ClusterNetworkUp, _CLUSTER_NETWORK_STATE, _CLUSTER_NETWORK_STATE enumeration [Failover Cluster], clusapi/CLUSTER_NETWORK_STATE, clusapi/ClusterNetworkDown, clusapi/ClusterNetworkPartitioned, clusapi/ClusterNetworkStateUnknown, clusapi/ClusterNetworkUnavailable, clusapi/ClusterNetworkUp, clusapi/_CLUSTER_NETWORK_STATE, msclus/CLUSTER_NETWORK_STATE, msclus/ClusterNetworkDown, msclus/ClusterNetworkPartitioned, msclus/ClusterNetworkStateUnknown, msclus/ClusterNetworkUnavailable, msclus/ClusterNetworkUp, msclus/_CLUSTER_NETWORK_STATE, mscs.cluster_network_state
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
req.typenames: CLUSTER_NETWORK_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_NETWORK_STATE
 - clusapi/CLUSTER_NETWORK_STATE
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
 - CLUSTER_NETWORK_STATE
---

# CLUSTER_NETWORK_STATE enumeration


## -description

Enumerates the possible values of the state of a 
    <a href="/previous-versions/windows/desktop/mscs/networks">network</a>.

## -enum-fields

### -field ClusterNetworkStateUnknown:-1

The operation was not successful. For more information about the error, call the function 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

### -field ClusterNetworkUnavailable

All of the network interfaces on the network are unavailable, which means that the nodes that own the network 
       interfaces are down.

### -field ClusterNetworkDown

The network is not operational; none of the <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> on the network 
       can communicate.

### -field ClusterNetworkPartitioned

The network is operational, but two or more nodes on the network cannot communicate. Typically a 
       path-specific problem has occurred.

### -field ClusterNetworkUp

The network is operational; all of the nodes in the cluster can communicate.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternetworkstate">GetClusterNetworkState</a>



<a href="/previous-versions/windows/desktop/mscs/clusnetwork-state">State Property of the ClusNetwork Object</a>
