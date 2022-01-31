---
UID: NE:clusapi.CLUSTER_NETINTERFACE_STATE
title: CLUSTER_NETINTERFACE_STATE (clusapi.h)
description: Enumerates the possible values of the state of a network interface.
helpviewer_keywords: ["CLUSTER_NETINTERFACE_STATE","CLUSTER_NETINTERFACE_STATE enumeration [Failover Cluster]","ClusterNetInterfaceFailed","ClusterNetInterfaceStateUnknown","ClusterNetInterfaceUnavailable","ClusterNetInterfaceUnreachable","ClusterNetInterfaceUp","_CLUSTER_NETINTERFACE_STATE","_CLUSTER_NETINTERFACE_STATE enumeration [Failover Cluster]","clusapi/CLUSTER_NETINTERFACE_STATE","clusapi/ClusterNetInterfaceFailed","clusapi/ClusterNetInterfaceStateUnknown","clusapi/ClusterNetInterfaceUnavailable","clusapi/ClusterNetInterfaceUnreachable","clusapi/ClusterNetInterfaceUp","clusapi/_CLUSTER_NETINTERFACE_STATE","msclus/CLUSTER_NETINTERFACE_STATE","msclus/ClusterNetInterfaceFailed","msclus/ClusterNetInterfaceStateUnknown","msclus/ClusterNetInterfaceUnavailable","msclus/ClusterNetInterfaceUnreachable","msclus/ClusterNetInterfaceUp","msclus/_CLUSTER_NETINTERFACE_STATE","mscs.cluster_netinterface_state"]
old-location: mscs\cluster_netinterface_state.htm
tech.root: MsCS
ms.assetid: 8b4dc26c-0bac-4ff1-b5ae-4524c81ccdf7
ms.date: 12/05/2018
ms.keywords: CLUSTER_NETINTERFACE_STATE, CLUSTER_NETINTERFACE_STATE enumeration [Failover Cluster], ClusterNetInterfaceFailed, ClusterNetInterfaceStateUnknown, ClusterNetInterfaceUnavailable, ClusterNetInterfaceUnreachable, ClusterNetInterfaceUp, _CLUSTER_NETINTERFACE_STATE, _CLUSTER_NETINTERFACE_STATE enumeration [Failover Cluster], clusapi/CLUSTER_NETINTERFACE_STATE, clusapi/ClusterNetInterfaceFailed, clusapi/ClusterNetInterfaceStateUnknown, clusapi/ClusterNetInterfaceUnavailable, clusapi/ClusterNetInterfaceUnreachable, clusapi/ClusterNetInterfaceUp, clusapi/_CLUSTER_NETINTERFACE_STATE, msclus/CLUSTER_NETINTERFACE_STATE, msclus/ClusterNetInterfaceFailed, msclus/ClusterNetInterfaceStateUnknown, msclus/ClusterNetInterfaceUnavailable, msclus/ClusterNetInterfaceUnreachable, msclus/ClusterNetInterfaceUp, msclus/_CLUSTER_NETINTERFACE_STATE, mscs.cluster_netinterface_state
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
req.typenames: CLUSTER_NETINTERFACE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_NETINTERFACE_STATE
 - clusapi/CLUSTER_NETINTERFACE_STATE
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
 - CLUSTER_NETINTERFACE_STATE
---

# CLUSTER_NETINTERFACE_STATE enumeration


## -description

Enumerates the possible values of the state of a 
    <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>.

## -enum-fields

### -field ClusterNetInterfaceStateUnknown:-1

The operation was not successful. For more information about the error, call the function 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternetinterfacestate">GetClusterNetInterfaceState</a>



<a href="/previous-versions/windows/desktop/mscs/clusnetinterface-state">State Property of the ClusNetInterface Object</a>
