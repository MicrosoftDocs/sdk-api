---
UID: NE:msclus.CLUSTER_RESOURCE_TYPE_ENUM
title: CLUSTER_RESOURCE_TYPE_ENUM
author: windows-driver-content
description: Describes the type of cluster object being enumerated by the ClusterResourceTypeEnum and ClusterResourceTypeOpenEnum functions.
old-location: mscs\cluster_resource_type_enum.htm
old-project: MsCS
ms.assetid: f8356cb3-303c-4294-a634-d91d5141004a
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: CLUSTER_RESOURCE_TYPE_ENUM, CLUSTER_RESOURCE_TYPE_ENUM enumeration [Failover Cluster], CLUSTER_RESOURCE_TYPE_ENUM_ALL, CLUSTER_RESOURCE_TYPE_ENUM_NODES, CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, _CLUSTER_RESOURCE_TYPE_ENUM, _CLUSTER_RESOURCE_TYPE_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_RESOURCE_TYPE_ENUM, clusapi/CLUSTER_RESOURCE_TYPE_ENUM_ALL, clusapi/CLUSTER_RESOURCE_TYPE_ENUM_NODES, clusapi/CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, clusapi/_CLUSTER_RESOURCE_TYPE_ENUM, msclus/CLUSTER_RESOURCE_TYPE_ENUM, msclus/CLUSTER_RESOURCE_TYPE_ENUM_ALL, msclus/CLUSTER_RESOURCE_TYPE_ENUM_NODES, msclus/CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, msclus/_CLUSTER_RESOURCE_TYPE_ENUM, mscs.cluster_resource_type_enum
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CLUSTER_RESOURCE_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusAPI.h
-	MsClus.h
api_name:
-	CLUSTER_RESOURCE_TYPE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

