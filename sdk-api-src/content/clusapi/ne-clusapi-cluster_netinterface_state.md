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

# CLUSTER_NETINTERFACE_STATE enumeration


## -description


Enumerates the possible values of the state of a 
    <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>.


## -enum-fields




### -field ClusterNetInterfaceStateUnknown

The operation was not successful. For more information about the error, call the function 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


### -field ClusterNetInterfaceUnavailable

The node that owns the network interface is down.


### -field ClusterNetInterfaceFailed

The network interface cannot communicate with any other network interface.


### -field ClusterNetInterfaceUnreachable

The network interface cannot communicate with at least one other network interface whose state is not 
      <b>ClusterNetInterfaceFailed</b> or 
      <b>ClusterNetInterfaceUnavailable</b>.


### -field ClusterNetInterfaceUp

The network interface can communicate with all other network interfaces whose state is not 
      <b>ClusterNetInterfaceFailed</b> or 
      <b>ClusterNetInterfaceUnavailable</b>.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/d84a5e3f-d0f9-4345-b008-e15c277dcbd5">GetClusterNetInterfaceState</a>



<a href="https://msdn.microsoft.com/3bc6bec3-bfe4-4ab4-8ad3-c42eba6d7cba">State Property of the ClusNetInterface Object</a>
 

 

