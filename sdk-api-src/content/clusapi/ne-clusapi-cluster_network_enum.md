---
UID: NE:clusapi.CLUSTER_NETWORK_ENUM
title: CLUSTER_NETWORK_ENUM (clusapi.h)
description: Describes the type of cluster object being enumerated by the ClusterNetworkEnum and ClusterNetworkOpenEnum functions.
helpviewer_keywords: ["CLUSTER_NETWORK_ENUM","CLUSTER_NETWORK_ENUM enumeration [Failover Cluster]","CLUSTER_NETWORK_ENUM_ALL","CLUSTER_NETWORK_ENUM_NETINTERFACES","_CLUSTER_NETWORK_ENUM","_CLUSTER_NETWORK_ENUM enumeration [Failover Cluster]","clusapi/CLUSTER_NETWORK_ENUM","clusapi/CLUSTER_NETWORK_ENUM_ALL","clusapi/CLUSTER_NETWORK_ENUM_NETINTERFACES","clusapi/_CLUSTER_NETWORK_ENUM","msclus/CLUSTER_NETWORK_ENUM","msclus/CLUSTER_NETWORK_ENUM_ALL","msclus/CLUSTER_NETWORK_ENUM_NETINTERFACES","msclus/_CLUSTER_NETWORK_ENUM","mscs.cluster_network_enum"]
old-location: mscs\cluster_network_enum.htm
tech.root: MsCS
ms.assetid: f5b02ce2-92d0-4ae7-a5bb-8e5d9c987095
ms.date: 12/05/2018
ms.keywords: CLUSTER_NETWORK_ENUM, CLUSTER_NETWORK_ENUM enumeration [Failover Cluster], CLUSTER_NETWORK_ENUM_ALL, CLUSTER_NETWORK_ENUM_NETINTERFACES, _CLUSTER_NETWORK_ENUM, _CLUSTER_NETWORK_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_NETWORK_ENUM, clusapi/CLUSTER_NETWORK_ENUM_ALL, clusapi/CLUSTER_NETWORK_ENUM_NETINTERFACES, clusapi/_CLUSTER_NETWORK_ENUM, msclus/CLUSTER_NETWORK_ENUM, msclus/CLUSTER_NETWORK_ENUM_ALL, msclus/CLUSTER_NETWORK_ENUM_NETINTERFACES, msclus/_CLUSTER_NETWORK_ENUM, mscs.cluster_network_enum
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
req.typenames: CLUSTER_NETWORK_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_NETWORK_ENUM
 - clusapi/CLUSTER_NETWORK_ENUM
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
 - CLUSTER_NETWORK_ENUM
---

# CLUSTER_NETWORK_ENUM enumeration


## -description

Describes the type of cluster object being enumerated by the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkenum">ClusterNetworkEnum</a> and 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkopenenum">ClusterNetworkOpenEnum</a> functions.

## -enum-fields

### -field CLUSTER_NETWORK_ENUM_NETINTERFACES:0x00000001

The object is a <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>.

### -field CLUSTER_NETWORK_ENUM_ALL

All cluster objects on the network.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkenum">ClusterNetworkEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkopenenum">ClusterNetworkOpenEnum</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
