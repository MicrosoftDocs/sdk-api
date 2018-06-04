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
 

 

