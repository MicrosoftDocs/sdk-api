---
UID: NC:clusapi.PCLUSAPI_CLUSTER_ENUM
title: PCLUSAPI_CLUSTER_ENUM
author: windows-driver-content
description: Enumerates the cluster objects in a cluster, returning the name of one object with each call.
old-location: mscs\clusterenum.htm
old-project: MsCS
ms.assetid: a7511ac6-04cb-407b-90aa-3382c5160cb6
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: CLUSTER_ENUM_ALL, CLUSTER_ENUM_GROUP, CLUSTER_ENUM_INTERNAL_NETWORK, CLUSTER_ENUM_NETINTERFACE, CLUSTER_ENUM_NETWORK, CLUSTER_ENUM_NODE, CLUSTER_ENUM_RESOURCE, CLUSTER_ENUM_RESTYPE, CLUSTER_ENUM_SHARED_VOLUME_RESOURCE, PCLUSAPI_CLUSTER_ENUM, PCLUSAPI_CLUSTER_ENUM callback, PCLUSAPI_CLUSTER_ENUM callback function [Failover Cluster], _wolf_clusterenum, clusapi/PCLUSAPI_CLUSTER_ENUM, mscs.clusterenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_ENUM callback function


## -description


Enumerates the <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>, returning the name of one object with each 
    call. The <b>PCLUSAPI_CLUSTER_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hEnum [in]

A cluster enumeration handle returned by the 
       <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a> function.


### -param dwIndex [in]

The index used to identify the next entry to be enumerated. This parameter should be zero for the first call 
       to <i>ClusterEnum</i> and then incremented for subsequent 
       calls.


### -param lpdwType [out]

A pointer to the type of object returned. One of the following values of the 
       <a href="https://msdn.microsoft.com/e3d5a207-d30e-4935-be95-0957e68d4fe6">CLUSTER_ENUM</a> enumeration is returned with each call.



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

Enumerates all <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a>.


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



The <i>ClusterEnum</i> function is typically used to iterate 
     through a collection of <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> of one 
     or more types. If, for example, an application wants to enumerate all of the 
     <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> in a cluster, it calls 
     <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a> to open a cluster 
     enumerator that can process nodes. The <i>dwType</i> parameter is set to 
     <b>CLUSTER_ENUM_NODE</b> to specify nodes as the object type to be enumerated. If the 
     application enumerates <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> in addition to nodes, the 
     <i>dwType</i> parameter is set to 
     <code>CLUSTER_ENUM_NODE | CLUSTER_ENUM_GROUP</code>. With the handle that 
     <i>ClusterOpenEnum</i> returns, the application calls 
     <i>ClusterEnum</i> repeatedly to retrieve each of the objects. 
     The <i>lpdwType</i> parameter points to the type of object that is retrieved.

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more 
     information on sizing buffers, see 
     <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.


#### Examples

See <a href="https://msdn.microsoft.com/391b87d1-6765-45fd-bd27-37a1127e639a">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3d7e45a0-d580-4d14-8795-2418bba40c73">ClusterCloseEnum</a>



<a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a>



<a href="https://msdn.microsoft.com/538e5024-6c51-4b11-a5ff-9df6aa7a4606">SetClusterNetworkPriorityOrder</a>
 

 

