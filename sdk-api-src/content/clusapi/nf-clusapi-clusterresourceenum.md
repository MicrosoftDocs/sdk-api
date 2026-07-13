---
UID: NF:clusapi.ClusterResourceEnum
title: ClusterResourceEnum function (clusapi.h)
description: Enumerates a resource's dependent resources, nodes, or both.
helpviewer_keywords: ["CLUSTER_RESOURCE_ENUM_DEPENDS","CLUSTER_RESOURCE_ENUM_NODES","CLUSTER_RESOURCE_ENUM_PROVIDES","ClusterResourceEnum","ClusterResourceEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_ENUM","PCLUSAPI_CLUSTER_RESOURCE_ENUM function [Failover Cluster]","_wolf_clusterresourceenum","clusapi/ClusterResourceEnum","clusapi/PCLUSAPI_CLUSTER_RESOURCE_ENUM","mscs.clusterresourceenum"]
old-location: mscs\clusterresourceenum.htm
tech.root: MsCS
ms.assetid: 73627594-90df-496d-8120-b24c34f13fb5
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_ENUM_DEPENDS, CLUSTER_RESOURCE_ENUM_NODES, CLUSTER_RESOURCE_ENUM_PROVIDES, ClusterResourceEnum, ClusterResourceEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_ENUM function [Failover Cluster], _wolf_clusterresourceenum, clusapi/ClusterResourceEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_ENUM, mscs.clusterresourceenum
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
 - ClusterResourceEnum
 - clusapi/ClusterResourceEnum
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterResourceEnum
---

# ClusterResourceEnum function


## -description

Enumerates a <a href="/previous-versions/windows/desktop/mscs/resources">resource's</a> dependent resources, 
    <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a>, or both. It returns the name of one 
    <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a> with each call. The <b>PCLUSAPI_CLUSTER_RESOURCE_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hResEnum [in]

A resource enumeration handle returned from 
       the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a> function.

### -param dwIndex [in]

The index of the resource or node object to return. This parameter should be zero for the first call to the 
       <b>ClusterResourceEnum</b> function and then 
       incremented for subsequent calls.

### -param lpdwType [out]

The type of object returned by 
       <b>ClusterResourceEnum</b>.


The possible values are one of the following <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_enum">CLUSTER_RESOURCE_ENUM</a> enumeration values:





#### CLUSTER_RESOURCE_ENUM_DEPENDS (1)

The object is a resource and  <i>hResEnum</i> is a resource that depends on this object.



#### CLUSTER_RESOURCE_ENUM_PROVIDES (2)

The object is a resource that depends on the resource identified by <i>hResEnum</i>.



#### CLUSTER_RESOURCE_ENUM_NODES (4)

The object is a node that can host the resource identified by <i>hResEnum</i>.

### -param lpszName [out]

A pointer to a null-terminated Unicode string containing the name of the returned object.

### -param lpcchName [in, out]

A pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating null character. On 
       output, specifies the number of characters in the resulting name, excluding the terminating null character.

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
The operation completed successfully or the <i>lpszName</i> parameter is 
         <b>NULL</b>.

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
The buffer pointed to by the <i>lpszName</i> parameter is not big enough to hold the 
         result. The <i>lpcchName</i> parameter returns the number of characters in the result, 
         excluding the terminating null character.

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
There are no more objects to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/Debug/system-error-codes">System error code</a></b></dt>
</dl>
</td>
<td width="60%">
Any other returned error code indicates that the operation failed.

</td>
</tr>
</table>

## -remarks

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating null character in the count. For more information on 
     sizing buffers, see <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.

Do not call <b>ClusterResourceEnum</b> from any 
     resource DLL entry point function. 
     <b>ClusterResourceEnum</b> can safely be called from a 
     worker thread. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Cluster Resource Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecloseenum">ClusterResourceCloseEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a>