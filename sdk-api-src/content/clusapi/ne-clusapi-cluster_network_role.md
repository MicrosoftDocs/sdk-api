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

# CLUSTER_NETWORK_ROLE enumeration


## -description


Describes the role a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a> plays in the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>. The 
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
 

 

