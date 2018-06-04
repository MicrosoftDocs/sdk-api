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

# CLUSTER_NODE_STATE enumeration


## -description


Describes the state of a cluster node. The 
    <a href="https://msdn.microsoft.com/94c83582-3d99-4a20-ad58-1af4e8190781">GetClusterNodeState</a> and 
    <a href="https://msdn.microsoft.com/c1887055-518a-4177-a618-418c75883d69">State</a> properties use this enumeration.


## -enum-fields




### -field ClusterNodeStateUnknown

The operation was not successful. For more information about the error, call the function 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


### -field ClusterNodeUp

The node is physically plugged in, turned on, booted, and capable of executing programs. This value is also 
       used by the 
       <a href="https://msdn.microsoft.com/4afadb62-2bea-46ef-b0d6-e327ac96d16f">SetClusterServiceAccountPassword</a> 
       function and <a href="https://msdn.microsoft.com/74e465e2-1328-4e05-b287-3ce27359c67a">Resume</a> method.


### -field ClusterNodeDown

The node is turned off or not operational.


### -field ClusterNodePaused

The node is running but not participating in cluster operations. This value is also used by the 
       <a href="https://msdn.microsoft.com/23b4ff74-f72f-4227-9b69-ff36fa6ed55b">PauseClusterNode</a> and 
       <a href="https://msdn.microsoft.com/4afadb62-2bea-46ef-b0d6-e327ac96d16f">SetClusterServiceAccountPassword</a> 
       functions. This value is also used <a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a> method.


### -field ClusterNodeJoining

The node is in the process of joining a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/94c83582-3d99-4a20-ad58-1af4e8190781">GetClusterNodeState</a>



<a href="https://msdn.microsoft.com/2fd16dda-b554-47fa-a040-15c7685d6392">Pause Method of the ClusNode Object</a>



<a href="https://msdn.microsoft.com/23b4ff74-f72f-4227-9b69-ff36fa6ed55b">PauseClusterNode</a>



<a href="https://msdn.microsoft.com/4afadb62-2bea-46ef-b0d6-e327ac96d16f">SetClusterServiceAccountPassword</a>



<a href="https://msdn.microsoft.com/c1887055-518a-4177-a618-418c75883d69">State Property of the ClusNode Object</a>
 

 

