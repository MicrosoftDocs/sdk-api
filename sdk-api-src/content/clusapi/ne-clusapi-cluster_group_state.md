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

# CLUSTER_GROUP_STATE enumeration


## -description


Enumerates the possible states of a 
   <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>.


## -enum-fields




### -field ClusterGroupStateUnknown

The state of the group is unknown.


### -field ClusterGroupOnline

All of the resources in the group are <a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">online</a>.


### -field ClusterGroupOffline

All of the resources in the group are <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">offline</a> or 
      there are no resources in the group.


### -field ClusterGroupFailed

At least one <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> in the group has failed.


### -field ClusterGroupPartialOnline

At least one resource in the group is online. No resources are 
      <a href="p_gly.htm">pending</a> or 
      <a href="f_gly.htm">failed</a>.


### -field ClusterGroupPending

At least one resource in the group is in a pending state. There are no failed resources.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/5f794dee-aeee-4906-ba63-c154bfda4d17">GetClusterGroupState</a>



<a href="https://msdn.microsoft.com/7eb8662c-a6ca-46e5-99ee-84e0dd6b0961">State Property of the ClusResGroup Object</a>
 

 

