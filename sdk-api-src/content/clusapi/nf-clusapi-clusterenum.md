---
UID: NF:clusapi.ClusterEnum
title: ClusterEnum function
author: windows-sdk-content
description: Enumerates the cluster objects in a cluster, returning the name of one object with each call.
old-location: mscs\clusterenum.htm
tech.root: mscs
ms.assetid: a7511ac6-04cb-407b-90aa-3382c5160cb6
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CLUSTER_ENUM_ALL, CLUSTER_ENUM_GROUP, CLUSTER_ENUM_INTERNAL_NETWORK, CLUSTER_ENUM_NETINTERFACE, CLUSTER_ENUM_NETWORK, CLUSTER_ENUM_NODE, CLUSTER_ENUM_RESOURCE, CLUSTER_ENUM_RESTYPE, CLUSTER_ENUM_SHARED_VOLUME_RESOURCE, ClusterEnum, ClusterEnum function [Failover Cluster], PCLUSAPI_CLUSTER_ENUM, PCLUSAPI_CLUSTER_ENUM function [Failover Cluster], _wolf_clusterenum, clusapi/ClusterEnum, clusapi/PCLUSAPI_CLUSTER_ENUM, mscs.clusterenum
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
 - ClusterEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterEnum function


## -description


Enumerates the <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a> in a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>, returning the name of one object with each 
    call. The <b>PCLUSAPI_CLUSTER_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hEnum [in]

A cluster enumeration handle returned by the 
       <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a> function.


### -param dwIndex [in]

The index used to identify the next entry to be enumerated. This parameter should be zero for the first call 
       to <b>ClusterEnum</b> and then incremented for subsequent 
       calls.


### -param lpdwType [out]

A pointer to the type of object returned. One of the following values of the 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309146(v=VS.85).aspx">CLUSTER_ENUM</a> enumeration is returned with each call.



#### CLUSTER_ENUM_NODE (1 (0x1))

Enumerates the <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">nodes</a> in the cluster.



#### CLUSTER_ENUM_RESTYPE (2 (0x2))

Enumerates the <a href="https://msdn.microsoft.com/en-us/library/Aa372279(v=VS.85).aspx">resource types</a> in the cluster.



#### CLUSTER_ENUM_RESOURCE (4 (0x4))

Enumerates the <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resources</a> in the cluster.



#### CLUSTER_ENUM_GROUP (8 (0x8))

Enumerates the <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">groups</a> in the cluster.



#### CLUSTER_ENUM_NETWORK (16 (0x10))

Enumerates the <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">networks</a> in the cluster.



#### CLUSTER_ENUM_NETINTERFACE (32 (0x20))

Enumerates the <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interfaces</a> in the 
         cluster.



#### CLUSTER_ENUM_SHARED_VOLUME_RESOURCE (1073741824 (0x40000000))

Enumerates the cluster shared volumes used by the cluster.

<div class="alert"><b>Note</b>  Unlike most other enumeration bitmasks, this value must be used alone. Do not use the 
         <b>OR</b> operator to combine it with other bitmasks.</div>
<div> </div>
<b>Windows Server 2008:  </b>The <b>CLUSTER_ENUM_SHARED_VOLUME_RESOURCE</b> value is not supported before 
          Windows Server 2008 R2.



#### CLUSTER_ENUM_INTERNAL_NETWORK (2147483648 (0x80000000))

Enumerates the networks used by the cluster for internal communication. The networks are enumerated in 
         order of highest-to-lowest priority as established by 
         the <a href="https://msdn.microsoft.com/538e5024-6c51-4b11-a5ff-9df6aa7a4606">SetClusterNetworkPriorityOrder</a> 
         function.

<div class="alert"><b>Note</b>  Unlike most other enumeration bitmasks, this value must be used alone. Do not use the 
         <b>OR</b> operator to combine it with other bitmasks.</div>
<div> </div>


#### CLUSTER_ENUM_ALL ((CLUSTER_ENUM_NODE | CLUSTER_ENUM_RESTYPE | CLUSTER_ENUM_RESOURCE | CLUSTER_ENUM_GROUP | CLUSTER_ENUM_NETWORK | CLUSTER_ENUM_NETINTERFACE))

Enumerates all <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a>.


### -param lpszName [out]

A pointer to a null-terminated Unicode string containing the name of the returned object.


### -param lpcchName [in, out]

A pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.


## -returns



The function returns one of the following values.




## -remarks



The <b>ClusterEnum</b> function is typically used to iterate 
     through a collection of <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a> of one 
     or more types. If, for example, an application wants to enumerate all of the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">nodes</a> in a cluster, it calls 
     <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a> to open a cluster 
     enumerator that can process nodes. The <i>dwType</i> parameter is set to 
     <b>CLUSTER_ENUM_NODE</b> to specify nodes as the object type to be enumerated. If the 
     application enumerates <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">groups</a> in addition to nodes, the 
     <i>dwType</i> parameter is set to 
     <code>CLUSTER_ENUM_NODE | CLUSTER_ENUM_GROUP</code>. With the handle that 
     <b>ClusterOpenEnum</b> returns, the application calls 
     <b>ClusterEnum</b> repeatedly to retrieve each of the objects. 
     The <i>lpdwType</i> parameter points to the type of object that is retrieved.

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more 
     information on sizing buffers, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369338(v=VS.85).aspx">Data Size Conventions</a>.


#### Examples

See <a href="https://msdn.microsoft.com/en-us/library/Aa369563(v=VS.85).aspx">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3d7e45a0-d580-4d14-8795-2418bba40c73">ClusterCloseEnum</a>



<a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a>



<a href="https://msdn.microsoft.com/538e5024-6c51-4b11-a5ff-9df6aa7a4606">SetClusterNetworkPriorityOrder</a>
 

 

