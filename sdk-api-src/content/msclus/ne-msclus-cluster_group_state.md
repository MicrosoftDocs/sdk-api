---
UID: NE:msclus.CLUSTER_GROUP_STATE
title: CLUSTER_GROUP_STATE (msclus.h)
description: Enumerates the possible states of a group.
helpviewer_keywords: ["CLUSTER_GROUP_STATE","CLUSTER_GROUP_STATE enumeration [Failover Cluster]","ClusterGroupFailed","ClusterGroupOffline","ClusterGroupOnline","ClusterGroupPartialOnline","ClusterGroupPending","ClusterGroupStateUnknown","_CLUSTER_GROUP_STATE","_CLUSTER_GROUP_STATE enumeration [Failover Cluster]","clusapi/CLUSTER_GROUP_STATE","clusapi/ClusterGroupFailed","clusapi/ClusterGroupOffline","clusapi/ClusterGroupOnline","clusapi/ClusterGroupPartialOnline","clusapi/ClusterGroupPending","clusapi/ClusterGroupStateUnknown","clusapi/_CLUSTER_GROUP_STATE","msclus/CLUSTER_GROUP_STATE","msclus/ClusterGroupFailed","msclus/ClusterGroupOffline","msclus/ClusterGroupOnline","msclus/ClusterGroupPartialOnline","msclus/ClusterGroupPending","msclus/ClusterGroupStateUnknown","msclus/_CLUSTER_GROUP_STATE","mscs.cluster_group_state"]
old-location: mscs\cluster_group_state.htm
tech.root: MsCS
ms.assetid: 1dbc5494-a830-4ee7-b982-48792ad87c51
ms.date: 12/05/2018
ms.keywords: CLUSTER_GROUP_STATE, CLUSTER_GROUP_STATE enumeration [Failover Cluster], ClusterGroupFailed, ClusterGroupOffline, ClusterGroupOnline, ClusterGroupPartialOnline, ClusterGroupPending, ClusterGroupStateUnknown, _CLUSTER_GROUP_STATE, _CLUSTER_GROUP_STATE enumeration [Failover Cluster], clusapi/CLUSTER_GROUP_STATE, clusapi/ClusterGroupFailed, clusapi/ClusterGroupOffline, clusapi/ClusterGroupOnline, clusapi/ClusterGroupPartialOnline, clusapi/ClusterGroupPending, clusapi/ClusterGroupStateUnknown, clusapi/_CLUSTER_GROUP_STATE, msclus/CLUSTER_GROUP_STATE, msclus/ClusterGroupFailed, msclus/ClusterGroupOffline, msclus/ClusterGroupOnline, msclus/ClusterGroupPartialOnline, msclus/ClusterGroupPending, msclus/ClusterGroupStateUnknown, msclus/_CLUSTER_GROUP_STATE, mscs.cluster_group_state
req.header: msclus.h
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
targetos: Windows
req.typenames: CLUSTER_GROUP_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_GROUP_STATE
 - msclus/CLUSTER_GROUP_STATE
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
 - CLUSTER_GROUP_STATE
---

# CLUSTER_GROUP_STATE enumeration


## -description

Enumerates the possible states of a 
   <a href="/previous-versions/windows/desktop/mscs/groups">group</a>.

## -enum-fields

### -field ClusterGroupStateUnknown:-1

The state of the group is unknown.

### -field ClusterGroupOnline

All of the resources in the group are <a href="/previous-versions/windows/desktop/mscs/o-gly">online</a>.

### -field ClusterGroupOffline

All of the resources in the group are <a href="/previous-versions/windows/desktop/mscs/o-gly">offline</a> or 
      there are no resources in the group.

### -field ClusterGroupFailed

At least one <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> in the group has failed.

### -field ClusterGroupPartialOnline

At least one resource in the group is online. No resources are 
      <a href="/previous-versions/windows/desktop/mscs/p-gly">pending</a> or 
      <a href="/previous-versions/windows/desktop/mscs/f-gly">failed</a>.

### -field ClusterGroupPending

At least one resource in the group is in a pending state. There are no failed resources.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclustergroupstate">GetClusterGroupState</a>



<a href="/previous-versions/windows/desktop/mscs/clusresgroup-state">State Property of the ClusResGroup Object</a>
