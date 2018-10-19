---
UID: NE:clusapi.CLUSTER_RESOURCE_CREATE_FLAGS
title: CLUSTER_RESOURCE_CREATE_FLAGS
author: windows-sdk-content
description: Determines which resource monitor a given resource will be assigned to.
old-location: mscs\cluster_resource_create_flags.htm
tech.root: mscs
ms.assetid: 16f5ab58-2507-431a-98f9-bd00a24485ba
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CLUSTER_RESOURCE_CREATE_FLAGS, CLUSTER_RESOURCE_CREATE_FLAGS enumeration [Failover Cluster], CLUSTER_RESOURCE_DEFAULT_MONITOR, CLUSTER_RESOURCE_SEPARATE_MONITOR, CLUSTER_RESOURCE_VALID_FLAGS, _CLUSTER_RESOURCE_CREATE_FLAGS, _CLUSTER_RESOURCE_CREATE_FLAGS enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_CREATE_FLAGS, clusapi/CLUSTER_RESOURCE_DEFAULT_MONITOR, clusapi/CLUSTER_RESOURCE_SEPARATE_MONITOR, clusapi/CLUSTER_RESOURCE_VALID_FLAGS, clusapi/_CLUSTER_RESOURCE_CREATE_FLAGS, msclus/CLUSTER_RESOURCE_CREATE_FLAGS, msclus/CLUSTER_RESOURCE_DEFAULT_MONITOR, msclus/CLUSTER_RESOURCE_SEPARATE_MONITOR, msclus/CLUSTER_RESOURCE_VALID_FLAGS, msclus/_CLUSTER_RESOURCE_CREATE_FLAGS, mscs.cluster_resource_create_flags
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
 - CLUSTER_RESOURCE_CREATE_FLAGS
product: Windows
targetos: Windows
req.typenames: CLUSTER_RESOURCE_CREATE_FLAGS
req.redist: 
---

# CLUSTER_RESOURCE_CREATE_FLAGS enumeration


## -description


Determines which resource monitor a given resource will be assigned to.


## -enum-fields




### -field CLUSTER_RESOURCE_DEFAULT_MONITOR

The <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> determines the 
      <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> to which the new resource will be 
      assigned.


### -field CLUSTER_RESOURCE_SEPARATE_MONITOR

Causes the Cluster service to create a separate Resource Monitor dedicated exclusively to the new 
      resource.


### -field CLUSTER_RESOURCE_VALID_FLAGS

Contains all valid flags for the 
      <a href="https://msdn.microsoft.com/16f5ab58-2507-431a-98f9-bd00a24485ba">CLUSTER_RESOURCE_CREATE_FLAGS</a> 
      enumeration.


## -see-also




<a href="https://msdn.microsoft.com/c9fe8fa8-57d7-4866-8113-694dc44dae22">CreateClusterResource</a>



<a href="https://msdn.microsoft.com/aaaf80c4-216e-4aaa-a674-3f24e0bfce7e">CreateItem Method of the ClusResDependencies Object</a>



<a href="https://msdn.microsoft.com/e696bee0-7ca4-47ec-a29a-b13e445a72de">CreateItem Method of the ClusResDependents Object</a>



<a href="https://msdn.microsoft.com/215482f4-4357-462b-bf67-109cc36e22b7">CreateItem Method of the ClusResTypeResources Object</a>



<a href="https://msdn.microsoft.com/3ff2d33b-08aa-445b-930e-7fbe589f6269">CreateItem Method of the ClusResources Object</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

