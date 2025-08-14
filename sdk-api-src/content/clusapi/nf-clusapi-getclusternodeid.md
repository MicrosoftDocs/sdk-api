---
UID: NF:clusapi.GetClusterNodeId
title: GetClusterNodeId function (clusapi.h)
description: Returns the unique identifier of a cluster node.
helpviewer_keywords: ["GetClusterNodeId","GetClusterNodeId function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_NODE_ID","PCLUSAPI_GET_CLUSTER_NODE_ID function [Failover Cluster]","_wolf_getclusternodeid","clusapi/GetClusterNodeId","clusapi/PCLUSAPI_GET_CLUSTER_NODE_ID","mscs.getclusternodeid"]
old-location: mscs\getclusternodeid.htm
tech.root: MsCS
ms.assetid: 976ca079-10f7-4e12-9033-07ea83e8c92a
ms.date: 12/05/2018
ms.keywords: GetClusterNodeId, GetClusterNodeId function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NODE_ID, PCLUSAPI_GET_CLUSTER_NODE_ID function [Failover Cluster], _wolf_getclusternodeid, clusapi/GetClusterNodeId, clusapi/PCLUSAPI_GET_CLUSTER_NODE_ID, mscs.getclusternodeid
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
 - GetClusterNodeId
 - clusapi/GetClusterNodeId
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - GetClusterNodeId
---

# GetClusterNodeId function


## -description

Returns the unique identifier of a cluster 
    <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>. The <b>PCLUSAPI_GET_CLUSTER_NODE_ID</b> type defines a pointer to this function.

## -parameters

### -param hNode [in, optional]

Handle to the node with the identifier to be returned or <b>NULL</b>. If 
       <i>hNode</i> is set to <b>NULL</b>, the node identifier for the node on 
       which the application is running is returned in the content of <i>lpszNodeId</i>.

### -param lpszNodeId [out]

This parameter points to a buffer that receives the unique ID of <i>hNode</i>, including 
       the terminating <b>NULL</b> character.

### -param lpcchName [in, out]

On input, pointer to the count of characters in the buffer pointed to by the 
       <i>lpszNodeId</i> parameter, including the <b>NULL</b> terminator. On 
       output, pointer to the count of characters stored in the buffer excluding the <b>NULL</b> 
       terminator.

## -returns

This function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are the 
       possible values:

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
         <i>lpszNodeId</i> is not long enough to hold the required number of characters. 
         <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternodeid">GetClusterNodeId</a> sets the content of 
         <i>lpcchName</i> to the required length.

</td>
</tr>
</table>

## -remarks

The <b>PCLUSAPI_GET_CLUSTER_NODE_ID</b> type defines a pointer to this function.

If <i>hNode</i> is set to <b>NULL</b> and the caller is running on an 
     active cluster node, the <b>GetClusterNodeId</b> function 
     returns the identifier of the node on which the application is running. Setting <i>hNode</i> 
     to <b>NULL</b> is a convenient way for 
     <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLLs</a> to determine the node identifier of the node 
     they are running on. The <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-getcurrentclusternodeid">GetCurrentClusterNodeId</a> 
     macro can be used instead of passing <b>NULL</b> for the <i>hNode</i> 
     parameter.

A cluster node identifier is a unique identifier that does not change even if the node's name is changed.

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing 
     buffers, see <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-getcurrentclusternodeid">GetCurrentClusterNodeId</a>



<a href="/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>
