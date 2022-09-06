---
UID: NE:msclus.CLUSTER_RESOURCE_STATE
title: CLUSTER_RESOURCE_STATE (msclus.h)
description: Describes the operational condition of a resource.
helpviewer_keywords: ["CLUSTER_RESOURCE_STATE","CLUSTER_RESOURCE_STATE enumeration [Failover Cluster]","ClusterResourceFailed","ClusterResourceInherited","ClusterResourceInitializing","ClusterResourceOffline","ClusterResourceOfflinePending","ClusterResourceOnline","ClusterResourceOnlinePending","ClusterResourcePending","ClusterResourceStateUnknown","_CLUSTER_RESOURCE_STATE","_CLUSTER_RESOURCE_STATE enumeration [Failover Cluster]","clusapi/CLUSTER_RESOURCE_STATE","clusapi/ClusterResourceFailed","clusapi/ClusterResourceInherited","clusapi/ClusterResourceInitializing","clusapi/ClusterResourceOffline","clusapi/ClusterResourceOfflinePending","clusapi/ClusterResourceOnline","clusapi/ClusterResourceOnlinePending","clusapi/ClusterResourcePending","clusapi/ClusterResourceStateUnknown","clusapi/_CLUSTER_RESOURCE_STATE","msclus/CLUSTER_RESOURCE_STATE","msclus/ClusterResourceFailed","msclus/ClusterResourceInherited","msclus/ClusterResourceInitializing","msclus/ClusterResourceOffline","msclus/ClusterResourceOfflinePending","msclus/ClusterResourceOnline","msclus/ClusterResourceOnlinePending","msclus/ClusterResourcePending","msclus/ClusterResourceStateUnknown","msclus/_CLUSTER_RESOURCE_STATE","mscs.cluster_resource_state"]
old-location: mscs\cluster_resource_state.htm
tech.root: MsCS
ms.assetid: bd5dee18-a06f-4e46-a27e-c907b1c25a68
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_STATE, CLUSTER_RESOURCE_STATE enumeration [Failover Cluster], ClusterResourceFailed, ClusterResourceInherited, ClusterResourceInitializing, ClusterResourceOffline, ClusterResourceOfflinePending, ClusterResourceOnline, ClusterResourceOnlinePending, ClusterResourcePending, ClusterResourceStateUnknown, _CLUSTER_RESOURCE_STATE, _CLUSTER_RESOURCE_STATE enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_STATE, clusapi/ClusterResourceFailed, clusapi/ClusterResourceInherited, clusapi/ClusterResourceInitializing, clusapi/ClusterResourceOffline, clusapi/ClusterResourceOfflinePending, clusapi/ClusterResourceOnline, clusapi/ClusterResourceOnlinePending, clusapi/ClusterResourcePending, clusapi/ClusterResourceStateUnknown, clusapi/_CLUSTER_RESOURCE_STATE, msclus/CLUSTER_RESOURCE_STATE, msclus/ClusterResourceFailed, msclus/ClusterResourceInherited, msclus/ClusterResourceInitializing, msclus/ClusterResourceOffline, msclus/ClusterResourceOfflinePending, msclus/ClusterResourceOnline, msclus/ClusterResourceOnlinePending, msclus/ClusterResourcePending, msclus/ClusterResourceStateUnknown, msclus/_CLUSTER_RESOURCE_STATE, mscs.cluster_resource_state
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
req.typenames: CLUSTER_RESOURCE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_RESOURCE_STATE
 - msclus/CLUSTER_RESOURCE_STATE
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
 - CLUSTER_RESOURCE_STATE
---

# CLUSTER_RESOURCE_STATE enumeration


## -description

Describes the operational condition of a resource. These values are used by the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterresourcestate">GetClusterResourceState</a> function, the 
    <b>State</b> property of the 
    <a href="/previous-versions/windows/desktop/cluswmi/mscluster-resource">MSCluster_Resource</a> class, and the 
    <a href="/previous-versions/windows/desktop/mscs/clusresource-state">State</a> property of the 
    <a href="/previous-versions/windows/desktop/mscs/clusresource-object">ClusResource</a> object.

## -enum-fields

### -field ClusterResourceStateUnknown:-1

The operation was not successful. For more information about the error, call the function 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

### -field ClusterResourceInherited

The resource has been inherited.

### -field ClusterResourceInitializing

The resource is performing initialization.

### -field ClusterResourceOnline

The resource is operational and functioning normally.

### -field ClusterResourceOffline

The resource is not operational.

### -field ClusterResourceFailed

The resource has <a href="/previous-versions/windows/desktop/mscs/f-gly">failed</a>.

### -field ClusterResourcePending:128

The resource is in the process of coming online or going 
       <a href="/previous-versions/windows/desktop/mscs/o-gly">offline</a>.

### -field ClusterResourceOnlinePending

The resource is in the process of coming online.

### -field ClusterResourceOfflinePending

The resource is in the process of going offline.

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-clus_maintenance_mode_infoex">CLUS_MAINTENANCE_MODE_INFOEX</a>



<a href="/windows/desktop/api/clusapi/ns-clusapi-clus_provider_state_change_info">CLUS_PROVIDER_STATE_CHANGE_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterresourcestate">GetClusterResourceState</a>



<a href="/previous-versions/windows/desktop/cluswmi/mscluster-resource">MSCluster_Resource</a>



<a href="/previous-versions/windows/desktop/mscs/clusresource-state">State Property of the ClusResource Object</a>
