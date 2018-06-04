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
 

 

