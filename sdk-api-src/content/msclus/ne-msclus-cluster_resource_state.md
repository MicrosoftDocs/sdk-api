---
UID: NE:msclus.CLUSTER_RESOURCE_STATE
title: CLUSTER_RESOURCE_STATE
author: windows-sdk-content
description: Describes the operational condition of a resource.
old-location: mscs\cluster_resource_state.htm
old-project: mscs
ms.assetid: bd5dee18-a06f-4e46-a27e-c907b1c25a68
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CLUSTER_RESOURCE_STATE, CLUSTER_RESOURCE_STATE enumeration [Failover Cluster], ClusterResourceFailed, ClusterResourceInherited, ClusterResourceInitializing, ClusterResourceOffline, ClusterResourceOfflinePending, ClusterResourceOnline, ClusterResourceOnlinePending, ClusterResourcePending, ClusterResourceStateUnknown, _CLUSTER_RESOURCE_STATE, _CLUSTER_RESOURCE_STATE enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_STATE, clusapi/ClusterResourceFailed, clusapi/ClusterResourceInherited, clusapi/ClusterResourceInitializing, clusapi/ClusterResourceOffline, clusapi/ClusterResourceOfflinePending, clusapi/ClusterResourceOnline, clusapi/ClusterResourceOnlinePending, clusapi/ClusterResourcePending, clusapi/ClusterResourceStateUnknown, clusapi/_CLUSTER_RESOURCE_STATE, msclus/CLUSTER_RESOURCE_STATE, msclus/ClusterResourceFailed, msclus/ClusterResourceInherited, msclus/ClusterResourceInitializing, msclus/ClusterResourceOffline, msclus/ClusterResourceOfflinePending, msclus/ClusterResourceOnline, msclus/ClusterResourceOnlinePending, msclus/ClusterResourcePending, msclus/ClusterResourceStateUnknown, msclus/_CLUSTER_RESOURCE_STATE, mscs.cluster_resource_state
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: CLUSTER_RESOURCE_STATE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# CLUSTER_RESOURCE_STATE enumeration


## -description


Describes the operational condition of a resource. These values are used by the 
    <a href="https://msdn.microsoft.com/c3897c96-743e-4753-8fef-b8defe4f2b00">GetClusterResourceState</a> function, the 
    <b>State</b> property of the 
    <a href="mscs.mscluster_resource">MSCluster_Resource</a> class, and the 
    <a href="https://msdn.microsoft.com/3bae66a8-cc45-49e6-acea-c506623b25bc">State</a> property of the 
    <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> object.


## -enum-fields




### -field ClusterResourceStateUnknown

The operation was not successful. For more information about the error, call the function 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


### -field ClusterResourceInherited

The resource has been inherited.


### -field ClusterResourceInitializing

The resource is performing initialization.


### -field ClusterResourceOnline

The resource is operational and functioning normally.


### -field ClusterResourceOffline

The resource is not operational.


### -field ClusterResourceFailed

The resource has <a href="f_gly.htm">failed</a>.


### -field ClusterResourcePending

The resource is in the process of coming online or going 
       <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">offline</a>.


### -field ClusterResourceOnlinePending

The resource is in the process of coming online.


### -field ClusterResourceOfflinePending

The resource is in the process of going offline.


## -see-also




<a href="https://msdn.microsoft.com/d68b187d-39c5-42d3-b268-d5061da257c4">CLUS_MAINTENANCE_MODE_INFOEX</a>



<a href="https://msdn.microsoft.com/53e25d02-6dfa-4a74-8ff3-01c868d2fd44">CLUS_PROVIDER_STATE_CHANGE_INFO</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/c3897c96-743e-4753-8fef-b8defe4f2b00">GetClusterResourceState</a>



<a href="mscs.mscluster_resource">MSCluster_Resource</a>



<a href="https://msdn.microsoft.com/3bae66a8-cc45-49e6-acea-c506623b25bc">State Property of the ClusResource Object</a>
 

 

