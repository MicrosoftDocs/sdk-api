---
UID: NF:clusapi.ClusterNodeEnum
title: ClusterNodeEnum function (clusapi.h)
description: Enumerates the network interfaces or groups installed on a node, returning the name of each with each call.
helpviewer_keywords: ["CLUSTER_NODE_ENUM_GROUPS","CLUSTER_NODE_ENUM_NETINTERFACES","ClusterNodeEnum","ClusterNodeEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_NODE_ENUM","PCLUSAPI_CLUSTER_NODE_ENUM function [Failover Cluster]","_wolf_clusternodeenum","clusapi/ClusterNodeEnum","clusapi/PCLUSAPI_CLUSTER_NODE_ENUM","mscs.clusternodeenum"]
old-location: mscs\clusternodeenum.htm
tech.root: MsCS
ms.assetid: e184ef8e-9ec6-4d84-a3d0-850298262b81
ms.date: 12/05/2018
ms.keywords: CLUSTER_NODE_ENUM_GROUPS, CLUSTER_NODE_ENUM_NETINTERFACES, ClusterNodeEnum, ClusterNodeEnum function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_ENUM, PCLUSAPI_CLUSTER_NODE_ENUM function [Failover Cluster], _wolf_clusternodeenum, clusapi/ClusterNodeEnum, clusapi/PCLUSAPI_CLUSTER_NODE_ENUM, mscs.clusternodeenum
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
 - ClusterNodeEnum
 - clusapi/ClusterNodeEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterNodeEnum
---

# ClusterNodeEnum function


## -description

Enumerates the <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interfaces</a> or 
    <a href="/previous-versions/windows/desktop/mscs/groups">groups</a> installed on a 
    <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>, returning the name of each with each call. The <b>PCLUSAPI_CLUSTER_NODE_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hNodeEnum [in]

Handle to an existing enumeration object originally returned by the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a> function.

### -param dwIndex [in]

Index used to identify the next entry to be enumerated. This parameter should be zero for the first call to 
       <b>ClusterNodeEnum</b> and then incremented for subsequent 
       calls.

### -param lpdwType [out]

Pointer to the type of object returned. The following value of the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_node_enum">CLUSTER_NODE_ENUM</a> enumeration is returned with each 
       call.



#### CLUSTER_NODE_ENUM_NETINTERFACES (1)

The object is a network interface.



#### CLUSTER_NODE_ENUM_GROUPS (0x00000002)

The object is a cluster group.

<b>Windows Server 2008:  </b>The <b>CLUSTER_NODE_ENUM_GROUPS</b> value is not supported before 
          Windows Server 2008 R2.

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

To use <b>ClusterNodeEnum</b>, applications first open a 
     node enumeration handle by calling 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a> with the 
     <i>dwType</i> parameter set to <b>CLUSTER_NODE_ENUM_NETINTERFACES</b>. 
     For more information, see <a href="/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

Note that the <i>lpcchName</i> parameter refers to a count of characters and not a count of 
     bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. 
     For more information on sizing buffers, see 
     <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodecloseenum">ClusterNodeCloseEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a>



<a href="/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>