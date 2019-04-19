---
UID: NF:clusapi.ClusterOpenEnum
title: ClusterOpenEnum function (clusapi.h)
author: windows-sdk-content
description: Opens an enumerator for iterating through cluster objects in a cluster.
old-location: mscs\clusteropenenum.htm
tech.root: MsCS
ms.assetid: b6eb5c03-dd6e-42ef-a020-cf0d61143040
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CLUSTER_ENUM_ALL, CLUSTER_ENUM_GROUP, CLUSTER_ENUM_INTERNAL_NETWORK, CLUSTER_ENUM_NETINTERFACE, CLUSTER_ENUM_NETWORK, CLUSTER_ENUM_NODE, CLUSTER_ENUM_RESOURCE, CLUSTER_ENUM_RESTYPE, CLUSTER_ENUM_SHARED_VOLUME_RESOURCE, ClusterOpenEnum, ClusterOpenEnum function [Failover Cluster], PCLUSAPI_CLUSTER_OPEN_ENUM, PCLUSAPI_CLUSTER_OPEN_ENUM function [Failover Cluster], _wolf_clusteropenenum, clusapi/ClusterOpenEnum, clusapi/PCLUSAPI_CLUSTER_OPEN_ENUM, mscs.clusteropenenum
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
 - ClusterOpenEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterOpenEnum function


## -description


Opens an enumerator for iterating through 
    <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> in a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>. The 
    <b>PCLUSAPI_CLUSTER_OPEN_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

A handle to a cluster.


### -param dwType [in]

A bitmask that describes the type of objects to be enumerated. One or more of the following values of the 
       <a href="https://msdn.microsoft.com/e3d5a207-d30e-4935-be95-0957e68d4fe6">CLUSTER_ENUM</a> enumeration are valid.



#### CLUSTER_ENUM_NODE (1 (0x1))

Enumerates the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> in the cluster.



#### CLUSTER_ENUM_RESTYPE (2 (0x2))

Enumerates the <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource types</a> in the cluster.



#### CLUSTER_ENUM_RESOURCE (4 (0x4))

Enumerates the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> in the cluster.



#### CLUSTER_ENUM_GROUP (8 (0x8))

Enumerates the <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> in the cluster.



#### CLUSTER_ENUM_NETWORK (16 (0x10))

Enumerates the <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">networks</a> in the cluster.



#### CLUSTER_ENUM_NETINTERFACE (32 (0x20))

Enumerates the <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a> in the 
         cluster.



#### CLUSTER_ENUM_SHARED_VOLUME_RESOURCE (1073741824 (0x40000000))

Enumerates the cluster shared volumes that are used by the cluster.

<div class="alert"><b>Note</b>  Unlike most other enumeration bitmasks, this value must be used alone. Do not use the 
         <b>OR</b> operator to combine it with other bitmasks.</div>
<div> </div>
<b>Windows Server 2008:  </b>The <b>CLUSTER_ENUM_SHARED_VOLUME_RESOURCE</b> value is not supported before 
          Windows Server 2008 R2.



#### CLUSTER_ENUM_INTERNAL_NETWORK (2147483648 (0x80000000))

Enumerates the networks that are used by the cluster for internal communication. The networks are enumerated in 
         order of highest-to-lowest priority as established by 
         <a href="https://msdn.microsoft.com/538e5024-6c51-4b11-a5ff-9df6aa7a4606">SetClusterNetworkPriorityOrder</a>.

<div class="alert"><b>Note</b>  Unlike most other enumeration bitmasks, this value must be used alone. Do not use the 
         <b>OR</b> operator to combine it with other bitmasks.</div>
<div> </div>


#### CLUSTER_ENUM_ALL ((CLUSTER_ENUM_NODE | CLUSTER_ENUM_RESTYPE | CLUSTER_ENUM_RESOURCE | CLUSTER_ENUM_GROUP | CLUSTER_ENUM_NETWORK | CLUSTER_ENUM_NETINTERFACE))

Enumerates all cluster objects.


## -returns



If the operation succeeds, <b>ClusterOpenEnum</b> 
       returns a handle to a cluster enumerator.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the function <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Applications call the <b>ClusterOpenEnum</b> function to 
     create a particular type of enumerator. 
     <b>ClusterOpenEnum</b> can create enumerators for iterating 
     through groups, nodes, resource types, resources, or all of these. For example, an application can call 
     <b>ClusterOpenEnum</b> to get an enumeration of all of the 
     nodes and groups in a cluster by specifying 
     <code>CLUSTER_ENUM_GROUP | CLUSTER_ENUM_NODE</code> in the 
     <i>dwType</i> parameter. 
     <b>ClusterOpenEnum</b> returns a handle that can be passed 
     to <a href="https://msdn.microsoft.com/a7511ac6-04cb-407b-90aa-3382c5160cb6">ClusterEnum</a> to access each of the cluster groups or 
     nodes and to <a href="https://msdn.microsoft.com/3d7e45a0-d580-4d14-8795-2418bba40c73">ClusterCloseEnum</a> to release the 
     enumerator.


#### Examples

See <a href="https://msdn.microsoft.com/391b87d1-6765-45fd-bd27-37a1127e639a">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Cluster Management Functions</a>



<a href="https://msdn.microsoft.com/3d7e45a0-d580-4d14-8795-2418bba40c73">ClusterCloseEnum</a>



<a href="https://msdn.microsoft.com/a7511ac6-04cb-407b-90aa-3382c5160cb6">ClusterEnum</a>



<a href="https://msdn.microsoft.com/538e5024-6c51-4b11-a5ff-9df6aa7a4606">SetClusterNetworkPriorityOrder</a>
 

 

