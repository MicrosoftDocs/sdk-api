---
UID: NF:clusapi.ClusterResourceTypeEnum
title: ClusterResourceTypeEnum function
author: windows-sdk-content
description: Enumerates a resource type's possible owner nodes or resources.
old-location: mscs\clusterresourcetypeenum.htm
old-project: mscs
ms.assetid: 956300f4-a7e8-4a8b-ab7e-e8fc3a37bf21
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: CLUSTER_RESOURCE_TYPE_ENUM_NODES, CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, ClusterResourceTypeEnum, ClusterResourceTypeEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM function [Failover Cluster], _wolf_clusterresourcetypeenum, clusapi/ClusterResourceTypeEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM, mscs.clusterresourcetypeenum
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
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
 - ClusterResourceTypeEnum
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterResourceTypeEnum function


## -description


Enumerates a <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type's</a> possible owner 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> or resources, returning the name of one node or 
    resource per call. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hResTypeEnum [in]

Resource type enumeration handle returned from 
       <a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a>.


### -param dwIndex [in]

Index of the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> or node object to return. This 
       parameter should be zero for the first call to 
       <b>ClusterResourceTypeEnum</b> and then 
       incremented for subsequent calls.


### -param lpdwType [out]

Type of object returned by 
       <b>ClusterResourceTypeEnum</b>. The following 
       values of the <a href="https://msdn.microsoft.com/f8356cb3-303c-4294-a634-d91d5141004a">CLUSTER_RESOURCE_TYPE_ENUM</a> 
       enumeration are valid.



#### CLUSTER_RESOURCE_TYPE_ENUM_NODES (1)

The object is a node that can be a possible owner of the resource type.



#### CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES (2)

The object is a resource that is an instance of the resource type.


### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the returned object.


### -param lpcchName [in, out]

Pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.


## -returns



The function returns one of the following values.




## -remarks



Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing 
     buffers, see <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.


#### Examples

See <a href="https://msdn.microsoft.com/391b87d1-6765-45fd-bd27-37a1127e639a">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f8356cb3-303c-4294-a634-d91d5141004a">CLUSTER_RESOURCE_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/c6524604-7a73-414c-95bb-dce9524f3295">ClusterResourceTypeCloseEnum</a>



<a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a>



<a href="https://msdn.microsoft.com/5bcb0411-d9c1-47e7-b799-5b1fcf2a9274">Resource Type Management Functions</a>
 

 

