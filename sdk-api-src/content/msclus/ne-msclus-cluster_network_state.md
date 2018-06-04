---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CLUSTER_NETWORK_STATE enumeration


## -description


Enumerates the possible values of the state of a 
    <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>.


## -enum-fields




### -field ClusterNetworkStateUnknown

The operation was not successful. For more information about the error, call the function 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


### -field ClusterNetworkUnavailable

All of the network interfaces on the network are unavailable, which means that the nodes that own the network 
       interfaces are down.


### -field ClusterNetworkDown

The network is not operational; none of the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> on the network 
       can communicate.


### -field ClusterNetworkPartitioned

The network is operational, but two or more nodes on the network cannot communicate. Typically a 
       path-specific problem has occurred.


### -field ClusterNetworkUp

The network is operational; all of the nodes in the cluster can communicate.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/7fdbc0cf-fa7b-4b48-bd3c-46f174fc514a">GetClusterNetworkState</a>



<a href="https://msdn.microsoft.com/abf1f90f-8044-40cf-b360-f80accb9cc58">State Property of the ClusNetwork Object</a>
 

 

