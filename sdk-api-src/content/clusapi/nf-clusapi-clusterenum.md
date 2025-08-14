---
UID: NF:clusapi.ClusterEnum
title: ClusterEnum function (clusapi.h)
description: Enumerates the cluster objects in a cluster, returning the name of one object with each call.
helpviewer_keywords: ["CLUSTER_ENUM_ALL","CLUSTER_ENUM_GROUP","CLUSTER_ENUM_INTERNAL_NETWORK","CLUSTER_ENUM_NETINTERFACE","CLUSTER_ENUM_NETWORK","CLUSTER_ENUM_NODE","CLUSTER_ENUM_RESOURCE","CLUSTER_ENUM_RESTYPE","CLUSTER_ENUM_SHARED_VOLUME_RESOURCE","ClusterEnum","ClusterEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_ENUM","PCLUSAPI_CLUSTER_ENUM function [Failover Cluster]","_wolf_clusterenum","clusapi/ClusterEnum","clusapi/PCLUSAPI_CLUSTER_ENUM","mscs.clusterenum"]
old-location: mscs\clusterenum.htm
tech.root: MsCS
ms.assetid: a7511ac6-04cb-407b-90aa-3382c5160cb6
ms.date: 12/05/2018
ms.keywords: CLUSTER_ENUM_ALL, CLUSTER_ENUM_GROUP, CLUSTER_ENUM_INTERNAL_NETWORK, CLUSTER_ENUM_NETINTERFACE, CLUSTER_ENUM_NETWORK, CLUSTER_ENUM_NODE, CLUSTER_ENUM_RESOURCE, CLUSTER_ENUM_RESTYPE, CLUSTER_ENUM_SHARED_VOLUME_RESOURCE, ClusterEnum, ClusterEnum function [Failover Cluster], PCLUSAPI_CLUSTER_ENUM, PCLUSAPI_CLUSTER_ENUM function [Failover Cluster], _wolf_clusterenum, clusapi/ClusterEnum, clusapi/PCLUSAPI_CLUSTER_ENUM, mscs.clusterenum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterEnum
 - clusapi/ClusterEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterEnum
---

# ClusterEnum function


## -description

Enumerates the <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> in a 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>, returning the name of one object with each 
    call. The <b>PCLUSAPI_CLUSTER_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hEnum [in]

A cluster enumeration handle returned by the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenum">ClusterOpenEnum</a> function.

### -param dwIndex [in]

The index used to identify the next entry to be enumerated. This parameter should be zero for the first call 
       to <b>ClusterEnum</b> and then incremented for subsequent 
       calls.

### -param lpdwType [out]

A pointer to the type of object returned. One of the following values of the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_enum">CLUSTER_ENUM</a> enumeration is returned with each call.



#### CLUSTER_ENUM_NODE (1 (0x1))

Enumerates the <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> in the cluster.



#### CLUSTER_ENUM_RESTYPE (2 (0x2))

Enumerates the <a href="/previous-versions/windows/desktop/mscs/resource-types">resource types</a> in the cluster.



#### CLUSTER_ENUM_RESOURCE (4 (0x4))

Enumerates the <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> in the cluster.



#### CLUSTER_ENUM_GROUP (8 (0x8))

Enumerates the <a href="/previous-versions/windows/desktop/mscs/groups">groups</a> in the cluster.



#### CLUSTER_ENUM_NETWORK (16 (0x10))

Enumerates the <a href="/previous-versions/windows/desktop/mscs/networks">networks</a> in the cluster.



#### CLUSTER_ENUM_NETINTERFACE (32 (0x20))

Enumerates the <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interfaces</a> in the 
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
         the <a href="/windows/desktop/api/clusapi/nf-clusapi-setclusternetworkpriorityorder">SetClusterNetworkPriorityOrder</a> 
         function.

<div class="alert"><b>Note</b>  Unlike most other enumeration bitmasks, this value must be used alone. Do not use the 
         <b>OR</b> operator to combine it with other bitmasks.</div>
<div> </div>


#### CLUSTER_ENUM_ALL ((CLUSTER_ENUM_NODE | CLUSTER_ENUM_RESTYPE | CLUSTER_ENUM_RESOURCE | CLUSTER_ENUM_GROUP | CLUSTER_ENUM_NETWORK | CLUSTER_ENUM_NETINTERFACE))

Enumerates all <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a>.

### -param lpszName [out]

A pointer to a null-terminated Unicode string containing the name of the returned object.

### -param lpcchName [in, out]

A pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.

## -returns

The function returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
<dt>259 (0x103)</dt>
</dl>
</td>
<td width="60%">
No more data is available. This value is returned if there are no more objects of the requested type to be 
         returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
More data is available. This value is returned if the buffer pointed to by 
         <i>lpszName</i> is not big enough to hold the result. The 
         <i>lpcchName</i> parameter returns the number of characters in the result, excluding the 
         terminating <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>ClusterEnum</b> function is typically used to iterate 
     through a collection of <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> of one 
     or more types. If, for example, an application wants to enumerate all of the 
     <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> in a cluster, it calls 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenum">ClusterOpenEnum</a> to open a cluster 
     enumerator that can process nodes. The <i>dwType</i> parameter is set to 
     <b>CLUSTER_ENUM_NODE</b> to specify nodes as the object type to be enumerated. If the 
     application enumerates <a href="/previous-versions/windows/desktop/mscs/groups">groups</a> in addition to nodes, the 
     <i>dwType</i> parameter is set to 
     <code>CLUSTER_ENUM_NODE | CLUSTER_ENUM_GROUP</code>. With the handle that 
     <b>ClusterOpenEnum</b> returns, the application calls 
     <b>ClusterEnum</b> repeatedly to retrieve each of the objects. 
     The <i>lpdwType</i> parameter points to the type of object that is retrieved.

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more 
     information on sizing buffers, see 
     <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clustercloseenum">ClusterCloseEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenum">ClusterOpenEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-setclusternetworkpriorityorder">SetClusterNetworkPriorityOrder</a>