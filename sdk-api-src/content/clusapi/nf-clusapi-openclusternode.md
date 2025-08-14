---
UID: NF:clusapi.OpenClusterNode
title: OpenClusterNode function (clusapi.h)
description: Opens a node and returns a handle to it. (OpenClusterNode)
helpviewer_keywords: ["OpenClusterNode","OpenClusterNode function [Failover Cluster]","PCLUSAPI_OPEN_CLUSTER_NODE","PCLUSAPI_OPEN_CLUSTER_NODE function [Failover Cluster]","_wolf_openclusternode","clusapi/OpenClusterNode","clusapi/PCLUSAPI_OPEN_CLUSTER_NODE","mscs.openclusternode"]
old-location: mscs\openclusternode.htm
tech.root: MsCS
ms.assetid: 7658a030-d4b2-407c-829f-61491b5907e6
ms.date: 12/05/2018
ms.keywords: OpenClusterNode, OpenClusterNode function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NODE, PCLUSAPI_OPEN_CLUSTER_NODE function [Failover Cluster], _wolf_openclusternode, clusapi/OpenClusterNode, clusapi/PCLUSAPI_OPEN_CLUSTER_NODE, mscs.openclusternode
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
 - OpenClusterNode
 - clusapi/OpenClusterNode
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
 - OpenClusterNode
---

# OpenClusterNode function


## -description

Opens a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> and returns a handle to it. The <b>PCLUSAPI_OPEN_CLUSTER_NODE</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> returned from the 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a> or 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterex">OpenClusterEx</a> functions.

### -param lpszNodeName [in]

Pointer to the NetBIOS name of an existing node. If the DNS name of the node is used, the 
      <b>OpenClusterNode</b> function will fail and 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
      <b>ERROR_CLUSTER_NODE_NOT_FOUND</b>.

## -returns

If the operation was successful, <b>OpenClusterNode</b> 
       returns a node handle.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusternode">CloseClusterNode</a>



<a href="/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterex">OpenClusterEx</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternodeex">OpenClusterNodeEx</a>
