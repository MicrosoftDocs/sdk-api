---
UID: NE:clusapi.CLUSTER_GROUP_STATE
title: CLUSTER_GROUP_STATE
author: windows-sdk-content
description: Enumerates the possible states of a group.
old-location: mscs\cluster_group_state.htm
tech.root: mscs
ms.assetid: 1dbc5494-a830-4ee7-b982-48792ad87c51
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CLUSTER_GROUP_STATE, CLUSTER_GROUP_STATE enumeration [Failover Cluster], ClusterGroupFailed, ClusterGroupOffline, ClusterGroupOnline, ClusterGroupPartialOnline, ClusterGroupPending, ClusterGroupStateUnknown, _CLUSTER_GROUP_STATE, _CLUSTER_GROUP_STATE enumeration [Failover Cluster], clusapi/CLUSTER_GROUP_STATE, clusapi/ClusterGroupFailed, clusapi/ClusterGroupOffline, clusapi/ClusterGroupOnline, clusapi/ClusterGroupPartialOnline, clusapi/ClusterGroupPending, clusapi/ClusterGroupStateUnknown, clusapi/_CLUSTER_GROUP_STATE, msclus/CLUSTER_GROUP_STATE, msclus/ClusterGroupFailed, msclus/ClusterGroupOffline, msclus/ClusterGroupOnline, msclus/ClusterGroupPartialOnline, msclus/ClusterGroupPending, msclus/ClusterGroupStateUnknown, msclus/_CLUSTER_GROUP_STATE, mscs.cluster_group_state
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CLUSTER_GROUP_STATE
product: Windows
targetos: Windows
req.typenames: CLUSTER_GROUP_STATE
req.redist: 
---

# CLUSTER_GROUP_STATE enumeration


## -description


Enumerates the possible states of a 
   <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a>.


## -enum-fields




### -field ClusterGroupStateUnknown

The state of the group is unknown.


### -field ClusterGroupOnline

All of the resources in the group are <a href="https://msdn.microsoft.com/en-us/library/Aa371781(v=VS.85).aspx">online</a>.


### -field ClusterGroupOffline

All of the resources in the group are <a href="https://msdn.microsoft.com/en-us/library/Aa371781(v=VS.85).aspx">offline</a> or 
      there are no resources in the group.


### -field ClusterGroupFailed

At least one <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> in the group has failed.


### -field ClusterGroupPartialOnline

At least one resource in the group is online. No resources are 
      <a href="https://msdn.microsoft.com/en-us/library/Aa371816(v=VS.85).aspx">pending</a> or 
      <a href="https://msdn.microsoft.com/en-us/library/Aa369590(v=VS.85).aspx">failed</a>.


### -field ClusterGroupPending

At least one resource in the group is in a pending state. There are no failed resources.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/5f794dee-aeee-4906-ba63-c154bfda4d17">GetClusterGroupState</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368721(v=VS.85).aspx">State Property of the ClusResGroup Object</a>
 

 

