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

# CLUSTER_RESOURCE_TYPE_ENUM enumeration


## -description


Describes the type of cluster object being enumerated by the 
    <a href="https://msdn.microsoft.com/956300f4-a7e8-4a8b-ab7e-e8fc3a37bf21">ClusterResourceTypeEnum</a> and 
    <a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a> 
    functions.


## -enum-fields




### -field CLUSTER_RESOURCE_TYPE_ENUM_NODES

The object is a node that can be a possible owner of the resource type.


### -field CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES

The object is a resource that is an instance of the resource type.

<b>Windows Server 2008:  </b>This value is not supported before Windows Server 2008 R2. To emulate this on earlier platforms, 
       enumerate all resources in the cluster (see the 
       <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a> function) and filter the results 
       using the <a href="https://msdn.microsoft.com/716d2174-5fa7-4868-9f33-ab6f815e6335">ResUtilResourceTypesEqual</a> 
       function. If the call is made on a system without ResUtils.dll, then use the steps mentioned in the Remarks 
       section of the <b>ResUtilResourceTypesEqual</b> 
       function.


### -field CLUSTER_RESOURCE_TYPE_ENUM_ALL

All cluster objects identified by the 
       <a href="https://msdn.microsoft.com/956300f4-a7e8-4a8b-ab7e-e8fc3a37bf21">ClusterResourceTypeEnum</a> and 
       <a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a> 
       functions.


## -see-also




<a href="https://msdn.microsoft.com/956300f4-a7e8-4a8b-ab7e-e8fc3a37bf21">ClusterResourceTypeEnum</a>



<a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

