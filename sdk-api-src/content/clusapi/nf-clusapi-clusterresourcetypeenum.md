---
UID: NF:clusapi.ClusterResourceTypeEnum
title: ClusterResourceTypeEnum function (clusapi.h)
description: Enumerates a resource type's possible owner nodes or resources.
helpviewer_keywords: ["CLUSTER_RESOURCE_TYPE_ENUM_NODES","CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES","ClusterResourceTypeEnum","ClusterResourceTypeEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM","PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM function [Failover Cluster]","_wolf_clusterresourcetypeenum","clusapi/ClusterResourceTypeEnum","clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM","mscs.clusterresourcetypeenum"]
old-location: mscs\clusterresourcetypeenum.htm
tech.root: MsCS
ms.assetid: 956300f4-a7e8-4a8b-ab7e-e8fc3a37bf21
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_TYPE_ENUM_NODES, CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, ClusterResourceTypeEnum, ClusterResourceTypeEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM function [Failover Cluster], _wolf_clusterresourcetypeenum, clusapi/ClusterResourceTypeEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM, mscs.clusterresourcetypeenum
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
 - ClusterResourceTypeEnum
 - clusapi/ClusterResourceTypeEnum
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
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterResourceTypeEnum
---

# ClusterResourceTypeEnum function


## -description

Enumerates a <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type's</a> possible owner 
    <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> or resources, returning the name of one node or 
    resource per call. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hResTypeEnum [in]

Resource type enumeration handle returned from 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeopenenum">ClusterResourceTypeOpenEnum</a>.

### -param dwIndex [in]

Index of the <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> or node object to return. This 
       parameter should be zero for the first call to 
       <b>ClusterResourceTypeEnum</b> and then 
       incremented for subsequent calls.

### -param lpdwType [out]

Type of object returned by 
       <b>ClusterResourceTypeEnum</b>. The following 
       values of the <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_type_enum">CLUSTER_RESOURCE_TYPE_ENUM</a> 
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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
<dt>259</dt>
</dl>
</td>
<td width="60%">
There are no more objects to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234</dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpszName</i> is not big enough to hold the result. The 
         <i>lpcchName</i> parameter returns the number of characters in the result, excluding the 
         terminating <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/Debug/system-error-codes">System error code</a></b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>

## -remarks

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing 
     buffers, see <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_type_enum">CLUSTER_RESOURCE_TYPE_ENUM</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecloseenum">ClusterResourceTypeCloseEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeopenenum">ClusterResourceTypeOpenEnum</a>



<a href="/previous-versions/windows/desktop/mscs/resource-type-management-functions">Resource Type Management Functions</a>