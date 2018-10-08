---
UID: NF:clusapi.ClusterResourceTypeEnum
title: ClusterResourceTypeEnum function
author: windows-sdk-content
description: Enumerates a resource type's possible owner nodes or resources.
old-location: mscs\clusterresourcetypeenum.htm
tech.root: MsCS
ms.assetid: 956300f4-a7e8-4a8b-ab7e-e8fc3a37bf21
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CLUSTER_RESOURCE_TYPE_ENUM_NODES, CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, ClusterResourceTypeEnum, ClusterResourceTypeEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM function [Failover Cluster], _wolf_clusterresourcetypeenum, clusapi/ClusterResourceTypeEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM, mscs.clusterresourcetypeenum
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ClusterResourceTypeEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceTypeEnum function


## -description


Enumerates a <a href="https://msdn.microsoft.com/en-us/library/Aa372279(v=VS.85).aspx">resource type's</a> possible owner 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">nodes</a> or resources, returning the name of one node or 
    resource per call. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hResTypeEnum [in]

Resource type enumeration handle returned from 
       <a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a>.


### -param dwIndex [in]

Index of the <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> or node object to return. This 
       parameter should be zero for the first call to 
       <b>ClusterResourceTypeEnum</b> and then 
       incremented for subsequent calls.


### -param lpdwType [out]

Type of object returned by 
       <b>ClusterResourceTypeEnum</b>. The following 
       values of the <a href="https://msdn.microsoft.com/en-us/library/Bb309170(v=VS.85).aspx">CLUSTER_RESOURCE_TYPE_ENUM</a> 
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
     buffers, see <a href="https://msdn.microsoft.com/en-us/library/Aa369338(v=VS.85).aspx">Data Size Conventions</a>.


#### Examples

See <a href="https://msdn.microsoft.com/en-us/library/Aa369563(v=VS.85).aspx">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309170(v=VS.85).aspx">CLUSTER_RESOURCE_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/c6524604-7a73-414c-95bb-dce9524f3295">ClusterResourceTypeCloseEnum</a>



<a href="https://msdn.microsoft.com/fa05875a-26c7-401d-ae81-1d204bfd7df1">ClusterResourceTypeOpenEnum</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372314(v=VS.85).aspx">Resource Type Management Functions</a>
 

 

