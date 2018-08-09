---
UID: NE:clusapi.CLUSTER_GROUP_STATE
title: CLUSTER_GROUP_STATE
author: windows-sdk-content
description: Enumerates the possible states of a group.
old-location: mscs\cluster_group_state.htm
old-project: mscs
ms.assetid: 1dbc5494-a830-4ee7-b982-48792ad87c51
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CLUSTER_GROUP_STATE, CLUSTER_GROUP_STATE enumeration [Failover Cluster], ClusterGroupFailed, ClusterGroupOffline, ClusterGroupOnline, ClusterGroupPartialOnline, ClusterGroupPending, ClusterGroupStateUnknown, _CLUSTER_GROUP_STATE, _CLUSTER_GROUP_STATE enumeration [Failover Cluster], clusapi/CLUSTER_GROUP_STATE, clusapi/ClusterGroupFailed, clusapi/ClusterGroupOffline, clusapi/ClusterGroupOnline, clusapi/ClusterGroupPartialOnline, clusapi/ClusterGroupPending, clusapi/ClusterGroupStateUnknown, clusapi/_CLUSTER_GROUP_STATE, msclus/CLUSTER_GROUP_STATE, msclus/ClusterGroupFailed, msclus/ClusterGroupOffline, msclus/ClusterGroupOnline, msclus/ClusterGroupPartialOnline, msclus/ClusterGroupPending, msclus/ClusterGroupStateUnknown, msclus/_CLUSTER_GROUP_STATE, mscs.cluster_group_state
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CLUSTER_GROUP_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_GROUP_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
      <a href="https://msdn.microsoft.com/en-us/library/Aa371816(v=VS.85).aspx">pending</a> or 
      <a href="https://msdn.microsoft.com/en-us/library/Aa369590(v=VS.85).aspx">failed</a>.


### -field ClusterGroupPending

At least one resource in the group is in a pending state. There are no failed resources.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/5f794dee-aeee-4906-ba63-c154bfda4d17">GetClusterGroupState</a>



<a href="https://msdn.microsoft.com/7eb8662c-a6ca-46e5-99ee-84e0dd6b0961">State Property of the ClusResGroup Object</a>
 

 

