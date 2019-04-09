---
UID: NE:clusapi.CLUSTER_NETWORK_ROLE
title: CLUSTER_NETWORK_ROLE (clusapi.h)
author: windows-sdk-content
description: Describes the role a network plays in the cluster.
old-location: mscs\cluster_network_role.htm
tech.root: MsCS
ms.assetid: 9c495cc4-d4d5-4465-9172-3171e55a14b0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CLUSTER_NETWORK_ROLE, CLUSTER_NETWORK_ROLE enumeration [Failover Cluster], ClusterNetworkRoleClientAccess, ClusterNetworkRoleInternalAndClient, ClusterNetworkRoleInternalUse, ClusterNetworkRoleNone, _CLUSTER_NETWORK_ROLE, _CLUSTER_NETWORK_ROLE enumeration [Failover Cluster], clusapi/CLUSTER_NETWORK_ROLE, clusapi/ClusterNetworkRoleClientAccess, clusapi/ClusterNetworkRoleInternalAndClient, clusapi/ClusterNetworkRoleInternalUse, clusapi/ClusterNetworkRoleNone, clusapi/_CLUSTER_NETWORK_ROLE, msclus/CLUSTER_NETWORK_ROLE, msclus/ClusterNetworkRoleClientAccess, msclus/ClusterNetworkRoleInternalAndClient, msclus/ClusterNetworkRoleInternalUse, msclus/ClusterNetworkRoleNone, msclus/_CLUSTER_NETWORK_ROLE, mscs.cluster_network_role
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
 - CLUSTER_NETWORK_ROLE
product: Windows
targetos: Windows
req.typenames: CLUSTER_NETWORK_ROLE
req.redist: 
---

# CLUSTER_NETWORK_ROLE enumeration


## -description


Describes the role a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a> plays in the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>. The 
    <a href="https://msdn.microsoft.com/1ab1382e-15ca-4438-afec-28bc5071c811">network role</a> and  
    <a href="https://msdn.microsoft.com/21ba6d5d-9a0f-4c60-9694-87a40dcb0c33">DefaultNetworkRole</a> common properties use 
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




<a href="https://msdn.microsoft.com/21ba6d5d-9a0f-4c60-9694-87a40dcb0c33">DefaultNetworkRole</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/1ab1382e-15ca-4438-afec-28bc5071c811">Network Role</a>
 

 

