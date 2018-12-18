---
UID: NF:clusapi.ClusterResourceTypeOpenEnum
title: ClusterResourceTypeOpenEnum function
author: windows-sdk-content
description: Opens an enumerator for iterating through a resource type's possible owner nodes or resources.
old-location: mscs\clusterresourcetypeopenenum.htm
tech.root: mscs
ms.assetid: fa05875a-26c7-401d-ae81-1d204bfd7df1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CLUSTER_RESOURCE_TYPE_ENUM_ALL, CLUSTER_RESOURCE_TYPE_ENUM_NODES, CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, ClusterResourceTypeOpenEnum, ClusterResourceTypeOpenEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM, PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM function [Failover Cluster], _wolf_clusterresourcetypeopenenum, clusapi/ClusterResourceTypeOpenEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM, mscs.clusterresourcetypeopenenum
ms.topic: function
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterResourceTypeOpenEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceTypeOpenEnum function


## -description


Opens an enumerator for iterating through a <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type's</a> 
    possible owner <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> or resources. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

<a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">Cluster</a> handle.


### -param lpszResourceTypeName [in]

A null-terminated Unicode string containing the name of the resource type.


### -param dwType [in]

Bitmask describing the type of <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> to be 
       enumerated. The following values of the <a href="https://msdn.microsoft.com/f8356cb3-303c-4294-a634-d91d5141004a">CLUSTER_RESOURCE_TYPE_ENUM</a> enumeration are valid.



#### CLUSTER_RESOURCE_TYPE_ENUM_NODES (1)

The object is a node that can be a possible owner of the resource type.



#### CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES (2)

The object is a resource that is an instance of the resource type.



#### CLUSTER_RESOURCE_TYPE_ENUM_ALL (3)

Enumerate both nodes and resources.


## -returns



If the operation succeeds, the function returns an enumeration handle which can be used in subsequent calls 
       to <a href="https://msdn.microsoft.com/956300f4-a7e8-4a8b-ab7e-e8fc3a37bf21">ClusterResourceTypeEnum</a>.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
      error, call the function <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/f8356cb3-303c-4294-a634-d91d5141004a">CLUSTER_RESOURCE_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/c6524604-7a73-414c-95bb-dce9524f3295">ClusterResourceTypeCloseEnum</a>



<a href="https://msdn.microsoft.com/956300f4-a7e8-4a8b-ab7e-e8fc3a37bf21">ClusterResourceTypeEnum</a>



<a href="https://msdn.microsoft.com/5bcb0411-d9c1-47e7-b799-5b1fcf2a9274">Resource Type Management Functions</a>
 

 

