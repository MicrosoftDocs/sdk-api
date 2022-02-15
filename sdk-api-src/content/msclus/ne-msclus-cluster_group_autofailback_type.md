---
UID: NE:msclus.CLUSTER_GROUP_AUTOFAILBACK_TYPE
title: CLUSTER_GROUP_AUTOFAILBACK_TYPE (msclus.h)
description: Used by the AutoFailbackType group common property to specify whether the group should be failed back to the node identified as its preferred owner when that node comes back online following a failover.
helpviewer_keywords: ["CGAFT","CGAFT enumeration [Failover Cluster]","CLUSTER_GROUP_AUTOFAILBACK_TYPE","CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration [Failover Cluster]","ClusterGroupAllowFailback","ClusterGroupFailbackTypeCount","ClusterGroupPreventFailback","_CLUSTER_GROUP_AUTOFAILBACK_TYPE","_CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration [Failover Cluster]","clusapi/CGAFT","clusapi/CLUSTER_GROUP_AUTOFAILBACK_TYPE","clusapi/ClusterGroupAllowFailback","clusapi/ClusterGroupFailbackTypeCount","clusapi/ClusterGroupPreventFailback","clusapi/_CLUSTER_GROUP_AUTOFAILBACK_TYPE","msclus/CGAFT","msclus/CLUSTER_GROUP_AUTOFAILBACK_TYPE","msclus/ClusterGroupAllowFailback","msclus/ClusterGroupFailbackTypeCount","msclus/ClusterGroupPreventFailback","msclus/_CLUSTER_GROUP_AUTOFAILBACK_TYPE","mscs.cluster_group_autofailback_type"]
old-location: mscs\cluster_group_autofailback_type.htm
tech.root: MsCS
ms.assetid: d7ba9298-25fc-454b-8583-196f84622cc5
ms.date: 12/05/2018
ms.keywords: CGAFT, CGAFT enumeration [Failover Cluster], CLUSTER_GROUP_AUTOFAILBACK_TYPE, CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration [Failover Cluster], ClusterGroupAllowFailback, ClusterGroupFailbackTypeCount, ClusterGroupPreventFailback, _CLUSTER_GROUP_AUTOFAILBACK_TYPE, _CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration [Failover Cluster], clusapi/CGAFT, clusapi/CLUSTER_GROUP_AUTOFAILBACK_TYPE, clusapi/ClusterGroupAllowFailback, clusapi/ClusterGroupFailbackTypeCount, clusapi/ClusterGroupPreventFailback, clusapi/_CLUSTER_GROUP_AUTOFAILBACK_TYPE, msclus/CGAFT, msclus/CLUSTER_GROUP_AUTOFAILBACK_TYPE, msclus/ClusterGroupAllowFailback, msclus/ClusterGroupFailbackTypeCount, msclus/ClusterGroupPreventFailback, msclus/_CLUSTER_GROUP_AUTOFAILBACK_TYPE, mscs.cluster_group_autofailback_type
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
targetos: Windows
req.typenames: CLUSTER_GROUP_AUTOFAILBACK_TYPE, CGAFT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_GROUP_AUTOFAILBACK_TYPE
 - msclus/CLUSTER_GROUP_AUTOFAILBACK_TYPE
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
 - CLUSTER_GROUP_AUTOFAILBACK_TYPE
---

# CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration


## -description

Used by the 
    <a href="/previous-versions/windows/desktop/mscs/groups-autofailbacktype">AutoFailbackType</a> group 
    <a href="/previous-versions/windows/desktop/mscs/common-properties">common property</a> to specify whether the group should be 
    failed back to the <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> identified as its preferred owner when that 
    node comes back online following a <a href="/previous-versions/windows/desktop/mscs/failover">failover</a>.

## -enum-fields

### -field ClusterGroupPreventFailback:0

Prevents <a href="/previous-versions/windows/desktop/mscs/failback">failback</a>.

### -field ClusterGroupAllowFailback

Allows failback (requires a preferred owners list for the group).

### -field ClusterGroupFailbackTypeCount

Defines a maximum group property value. It is not supported by the 
       <a href="/previous-versions/windows/desktop/mscs/groups-autofailbacktype">AutoFailbackType</a> group property.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/groups-autofailbacktype">AutoFailbackType</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/previous-versions/windows/desktop/mscs/common-properties">common property</a>
