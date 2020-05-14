---
UID: NE:msclus.CLUSTER_NETWORK_ROLE
title: CLUSTER_NETWORK_ROLE (msclus.h)
description: Describes the role a network plays in the cluster.helpviewer_keywords: ["CLUSTER_NETWORK_ROLE","CLUSTER_NETWORK_ROLE enumeration [Failover Cluster]","ClusterNetworkRoleClientAccess","ClusterNetworkRoleInternalAndClient","ClusterNetworkRoleInternalUse","ClusterNetworkRoleNone","_CLUSTER_NETWORK_ROLE","_CLUSTER_NETWORK_ROLE enumeration [Failover Cluster]","clusapi/CLUSTER_NETWORK_ROLE","clusapi/ClusterNetworkRoleClientAccess","clusapi/ClusterNetworkRoleInternalAndClient","clusapi/ClusterNetworkRoleInternalUse","clusapi/ClusterNetworkRoleNone","clusapi/_CLUSTER_NETWORK_ROLE","msclus/CLUSTER_NETWORK_ROLE","msclus/ClusterNetworkRoleClientAccess","msclus/ClusterNetworkRoleInternalAndClient","msclus/ClusterNetworkRoleInternalUse","msclus/ClusterNetworkRoleNone","msclus/_CLUSTER_NETWORK_ROLE","mscs.cluster_network_role"]
old-location: mscs\cluster_network_role.htm
tech.root: MsCS
ms.assetid: 9c495cc4-d4d5-4465-9172-3171e55a14b0
ms.date: 12/05/2018
ms.keywords: CLUSTER_NETWORK_ROLE, CLUSTER_NETWORK_ROLE enumeration [Failover Cluster], ClusterNetworkRoleClientAccess, ClusterNetworkRoleInternalAndClient, ClusterNetworkRoleInternalUse, ClusterNetworkRoleNone, _CLUSTER_NETWORK_ROLE, _CLUSTER_NETWORK_ROLE enumeration [Failover Cluster], clusapi/CLUSTER_NETWORK_ROLE, clusapi/ClusterNetworkRoleClientAccess, clusapi/ClusterNetworkRoleInternalAndClient, clusapi/ClusterNetworkRoleInternalUse, clusapi/ClusterNetworkRoleNone, clusapi/_CLUSTER_NETWORK_ROLE, msclus/CLUSTER_NETWORK_ROLE, msclus/ClusterNetworkRoleClientAccess, msclus/ClusterNetworkRoleInternalAndClient, msclus/ClusterNetworkRoleInternalUse, msclus/ClusterNetworkRoleNone, msclus/_CLUSTER_NETWORK_ROLE, mscs.cluster_network_role
f1_keywords:
- msclus/CLUSTER_NETWORK_ROLE
dev_langs:
- c++
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
- CLUSTER_NETWORK_ROLE
targetos: Windows
req.typenames: CLUSTER_NETWORK_ROLE
req.redist: 
ms.custom: 19H1
---

# CLUSTER_NETWORK_ROLE enumeration


## -description


Describes the role a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/networks">network</a> plays in the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/networks-role">network role</a> and  
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/clusters-defaultnetworkrole">DefaultNetworkRole</a> common properties use 
    this enumeration. This is a bitmask.


## -enum-fields




### -field ClusterNetworkRoleNone

The network is not used by the cluster.


### -field ClusterNetworkRoleInternalUse

The network is used to carry internal cluster communication.


### -field ClusterNetworkRoleClientAccess

Not supported.


### -field ClusterNetworkRoleInternalAndClient

The network is used to connect client systems and to carry internal cluster communication.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/clusters-defaultnetworkrole">DefaultNetworkRole</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/networks-role">Network Role</a>
 

 

