---
UID: NE:msclus.CLUSTER_NETINTERFACE_STATE
title: CLUSTER_NETINTERFACE_STATE
author: windows-sdk-content
description: Enumerates the possible values of the state of a network interface.
old-location: mscs\cluster_netinterface_state.htm
tech.root: mscs
ms.assetid: 8b4dc26c-0bac-4ff1-b5ae-4524c81ccdf7
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: CLUSTER_NETINTERFACE_STATE, CLUSTER_NETINTERFACE_STATE enumeration [Failover Cluster], ClusterNetInterfaceFailed, ClusterNetInterfaceStateUnknown, ClusterNetInterfaceUnavailable, ClusterNetInterfaceUnreachable, ClusterNetInterfaceUp, _CLUSTER_NETINTERFACE_STATE, _CLUSTER_NETINTERFACE_STATE enumeration [Failover Cluster], clusapi/CLUSTER_NETINTERFACE_STATE, clusapi/ClusterNetInterfaceFailed, clusapi/ClusterNetInterfaceStateUnknown, clusapi/ClusterNetInterfaceUnavailable, clusapi/ClusterNetInterfaceUnreachable, clusapi/ClusterNetInterfaceUp, clusapi/_CLUSTER_NETINTERFACE_STATE, msclus/CLUSTER_NETINTERFACE_STATE, msclus/ClusterNetInterfaceFailed, msclus/ClusterNetInterfaceStateUnknown, msclus/ClusterNetInterfaceUnavailable, msclus/ClusterNetInterfaceUnreachable, msclus/ClusterNetInterfaceUp, msclus/_CLUSTER_NETINTERFACE_STATE, mscs.cluster_netinterface_state
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_NETINTERFACE_STATE
product: Windows
targetos: Windows
req.typenames: CLUSTER_NETINTERFACE_STATE
req.redist: 
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
 

 

