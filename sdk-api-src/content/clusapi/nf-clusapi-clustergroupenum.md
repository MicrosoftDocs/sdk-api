---
UID: NF:clusapi.ClusterGroupEnum
title: ClusterGroupEnum function (clusapi.h)
description: Enumerates the resources in a group or the nodes that are the preferred owners of a group, returning the name of the resource or node with each call.
helpviewer_keywords: ["CLUSTER_GROUP_ENUM_CONTAINS","CLUSTER_GROUP_ENUM_NODES","ClusterGroupEnum","ClusterGroupEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_GROUP_ENUM","PCLUSAPI_CLUSTER_GROUP_ENUM function [Failover Cluster]","_wolf_clustergroupenum","clusapi/ClusterGroupEnum","clusapi/PCLUSAPI_CLUSTER_GROUP_ENUM","mscs.clustergroupenum"]
old-location: mscs\clustergroupenum.htm
tech.root: MsCS
ms.assetid: fffcae88-8df0-487f-9f6d-bc3560283ef1
ms.date: 12/05/2018
ms.keywords: CLUSTER_GROUP_ENUM_CONTAINS, CLUSTER_GROUP_ENUM_NODES, ClusterGroupEnum, ClusterGroupEnum function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_ENUM, PCLUSAPI_CLUSTER_GROUP_ENUM function [Failover Cluster], _wolf_clustergroupenum, clusapi/ClusterGroupEnum, clusapi/PCLUSAPI_CLUSTER_GROUP_ENUM, mscs.clustergroupenum
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
 - ClusterGroupEnum
 - clusapi/ClusterGroupEnum
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
 - ClusAPI.dll
api_name:
 - ClusterGroupEnum
---

# ClusterGroupEnum function


## -description

Enumerates the <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> in a 
    <a href="/previous-versions/windows/desktop/mscs/groups">group</a> or the <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> that 
    are the preferred owners of a group, returning the name of the resource or node with each call. The <b>PCLUSAPI_CLUSTER_GROUP_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hGroupEnum [in]

A group enumeration handle returned by the 
       <a href="/windows/win32/api/clusapi/nf-clusapi-clustergroupopenenum">ClusterGroupOpenEnum</a> function.

### -param dwIndex [in]

The index of the resource or node to return. This parameter should be zero for the first call to 
       <b>ClusterGroupEnum</b> and then incremented for 
       subsequent calls.

### -param lpdwType [out]

A pointer to the type of object returned by 
       <b>ClusterGroupEnum</b>. The following are valid values 
       of the <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_group_enum">CLUSTER_GROUP_ENUM</a> enumeration.



#### CLUSTER_GROUP_ENUM_CONTAINS (1)

The object is one of the resources in the group.



#### CLUSTER_GROUP_ENUM_NODES (2)

The object is one of the nodes in the preferred owners list of the group.

### -param lpszResourceName [out]

A pointer to a null-terminated Unicode string containing the name of the returned resource or node.

### -param lpcchName [in, out]

A pointer to the size of the <i>lpszResourceName</i> buffer as a count of characters. On 
       input, specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.

## -returns

The function can returns one of the following values.

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
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
More data is available. This value is returned if the buffer pointed to by 
         <i>lpszResourceName</i> is not big enough to hold the result. The 
         <i>lpcchName</i> parameter returns the number of characters in the result, excluding the 
         terminating <b>NULL</b>.

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
No more data is available. This value is returned if there are no more resources or nodes to be 
         returned.

</td>
</tr>
</table>
 

If the operation was not successful due to a problem other than those described with the 
       <b>ERROR_NO_MORE_ITEMS</b> or <b>ERROR_MORE_DATA</b> values, 
       <b>ClusterGroupEnum</b> returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more 
     information on sizing buffers, see 
     <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.

Do not call <b>ClusterGroupEnum</b> from any resource DLL 
     entry point function. <b>ClusterGroupEnum</b> can safely be 
     called from a worker thread. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupcloseenum">ClusterGroupCloseEnum</a>



<a href="/windows/win32/api/clusapi/nf-clusapi-clustergroupopenenum">ClusterGroupOpenEnum</a>



<a href="/previous-versions/windows/desktop/mscs/group-management-functions">Group Management Functions</a>