---
UID: NE:clusapi.CLUSTER_RESOURCE_RESTART_ACTION
title: CLUSTER_RESOURCE_RESTART_ACTION (clusapi.h)
description: Used by the RestartAction resource common property to specify the action to be taken by the cluster service if the resource fails.
helpviewer_keywords: ["CLUSTER_RESOURCE_RESTART_ACTION","CLUSTER_RESOURCE_RESTART_ACTION enumeration [Failover Cluster]","CRRA","CRRA enumeration [Failover Cluster]","ClusterResourceDontRestart","ClusterResourceRestartActionCount","ClusterResourceRestartNoNotify","ClusterResourceRestartNotify","_CLUSTER_RESOURCE_RESTART_ACTION","_CLUSTER_RESOURCE_RESTART_ACTION enumeration [Failover Cluster]","clusapi/CLUSTER_RESOURCE_RESTART_ACTION","clusapi/CRRA","clusapi/ClusterResourceDontRestart","clusapi/ClusterResourceRestartActionCount","clusapi/ClusterResourceRestartNoNotify","clusapi/ClusterResourceRestartNotify","clusapi/_CLUSTER_RESOURCE_RESTART_ACTION","msclus/CLUSTER_RESOURCE_RESTART_ACTION","msclus/CRRA","msclus/ClusterResourceDontRestart","msclus/ClusterResourceRestartActionCount","msclus/ClusterResourceRestartNoNotify","msclus/ClusterResourceRestartNotify","msclus/_CLUSTER_RESOURCE_RESTART_ACTION","mscs.cluster_resource_restart_action"]
old-location: mscs\cluster_resource_restart_action.htm
tech.root: MsCS
ms.assetid: 6300bdb7-2349-44f8-913a-dd84813bd3bd
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_RESTART_ACTION, CLUSTER_RESOURCE_RESTART_ACTION enumeration [Failover Cluster], CRRA, CRRA enumeration [Failover Cluster], ClusterResourceDontRestart, ClusterResourceRestartActionCount, ClusterResourceRestartNoNotify, ClusterResourceRestartNotify, _CLUSTER_RESOURCE_RESTART_ACTION, _CLUSTER_RESOURCE_RESTART_ACTION enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_RESTART_ACTION, clusapi/CRRA, clusapi/ClusterResourceDontRestart, clusapi/ClusterResourceRestartActionCount, clusapi/ClusterResourceRestartNoNotify, clusapi/ClusterResourceRestartNotify, clusapi/_CLUSTER_RESOURCE_RESTART_ACTION, msclus/CLUSTER_RESOURCE_RESTART_ACTION, msclus/CRRA, msclus/ClusterResourceDontRestart, msclus/ClusterResourceRestartActionCount, msclus/ClusterResourceRestartNoNotify, msclus/ClusterResourceRestartNotify, msclus/_CLUSTER_RESOURCE_RESTART_ACTION, mscs.cluster_resource_restart_action
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
req.typenames: CLUSTER_RESOURCE_RESTART_ACTION, CRRA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_RESOURCE_RESTART_ACTION
 - clusapi/CLUSTER_RESOURCE_RESTART_ACTION
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
 - CLUSTER_RESOURCE_RESTART_ACTION
---

# CLUSTER_RESOURCE_RESTART_ACTION enumeration


## -description

Used by the <a href="/previous-versions/windows/desktop/mscs/resources-restartaction">RestartAction</a> <a href="/previous-versions/windows/desktop/mscs/resource-common-properties">resource common property</a> to specify the action 
    to be taken by the <a href="/previous-versions/windows/desktop/mscs/cluster-service">cluster service</a> if the 
    <a href="/previous-versions/windows/desktop/mscs/resource-failure">resource fails</a>.

## -enum-fields

### -field ClusterResourceDontRestart:0

Do not restart the resource after a failure.

### -field ClusterResourceRestartNoNotify

Restart the resource after a failure. If the resource exceeds its restart threshold within its restart 
       period, do not attempt to <a href="/previous-versions/windows/desktop/mscs/failover">failover</a> the 
       <a href="/previous-versions/windows/desktop/mscs/groups">group</a> to another 
       <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> in the 
       <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

### -field ClusterResourceRestartNotify

Restart the resource after a failure. If the resource exceeds its restart threshold within its restart 
       period, attempt to fail over the group to another node in the cluster. This is the default setting.

### -field ClusterResourceRestartActionCount

Defines the maximum value of the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_restart_action">CLUSTER_RESOURCE_RESTART_ACTION</a> enumeration.  It is not a valid value for the 
       <a href="/previous-versions/windows/desktop/mscs/resources-restartaction">RestartAction</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/previous-versions/windows/desktop/mscs/resources-restartaction">RestartAction</a>



<a href="/previous-versions/windows/desktop/mscs/resource-common-properties">resource common property</a>
