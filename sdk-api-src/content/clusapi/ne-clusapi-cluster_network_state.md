---
UID: NE:clusapi.CLUSTER_NETWORK_STATE
title: CLUSTER_NETWORK_STATE
author: windows-sdk-content
description: Enumerates the possible values of the state of a network.
old-location: mscs\cluster_network_state.htm
tech.root: mscs
ms.assetid: 1a9e3ff0-eb5a-4a2e-ae19-e70213dc1a4a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CLUSTER_NETWORK_STATE, CLUSTER_NETWORK_STATE enumeration [Failover Cluster], ClusterNetworkDown, ClusterNetworkPartitioned, ClusterNetworkStateUnknown, ClusterNetworkUnavailable, ClusterNetworkUp, _CLUSTER_NETWORK_STATE, _CLUSTER_NETWORK_STATE enumeration [Failover Cluster], clusapi/CLUSTER_NETWORK_STATE, clusapi/ClusterNetworkDown, clusapi/ClusterNetworkPartitioned, clusapi/ClusterNetworkStateUnknown, clusapi/ClusterNetworkUnavailable, clusapi/ClusterNetworkUp, clusapi/_CLUSTER_NETWORK_STATE, msclus/CLUSTER_NETWORK_STATE, msclus/ClusterNetworkDown, msclus/ClusterNetworkPartitioned, msclus/ClusterNetworkStateUnknown, msclus/ClusterNetworkUnavailable, msclus/ClusterNetworkUp, msclus/_CLUSTER_NETWORK_STATE, mscs.cluster_network_state
ms.prod: windows
ms.technology: windows-sdk
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
 - CLUSTER_NETWORK_STATE
product: Windows
targetos: Windows
req.typenames: CLUSTER_NETWORK_STATE
req.redist: 
---

# CLUSTER_NETWORK_STATE enumeration


## -description


Enumerates the possible values of the state of a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a>.


## -enum-fields




### -field ClusterNetworkStateUnknown

The operation was not successful. For more information about the error, call the function 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


### -field ClusterNetworkUnavailable

All of the network interfaces on the network are unavailable, which means that the nodes that own the network 
       interfaces are down.


### -field ClusterNetworkDown

The network is not operational; none of the <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">nodes</a> on the network 
       can communicate.


### -field ClusterNetworkPartitioned

The network is operational, but two or more nodes on the network cannot communicate. Typically a 
       path-specific problem has occurred.


### -field ClusterNetworkUp

The network is operational; all of the nodes in the cluster can communicate.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/7fdbc0cf-fa7b-4b48-bd3c-46f174fc514a">GetClusterNetworkState</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa367984(v=VS.85).aspx">State Property of the ClusNetwork Object</a>
 

 

