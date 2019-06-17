---
UID: NF:clusapi.OpenClusterNode
title: OpenClusterNode function (clusapi.h)
author: windows-sdk-content
description: Opens a node and returns a handle to it.
old-location: mscs\openclusternode.htm
tech.root: MsCS
ms.assetid: 7658a030-d4b2-407c-829f-61491b5907e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OpenClusterNode, OpenClusterNode function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NODE, PCLUSAPI_OPEN_CLUSTER_NODE function [Failover Cluster], _wolf_openclusternode, clusapi/OpenClusterNode, clusapi/PCLUSAPI_OPEN_CLUSTER_NODE, mscs.openclusternode
ms.topic: function
f1_keywords: ["clusapi/OpenClusterNode"]
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
 - OpenClusterNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenClusterNode function


## -description


Opens a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a> and returns a handle to it. The <b>PCLUSAPI_OPEN_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/c-gly">cluster</a> returned from the 
      <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a> or 
      <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusterex">OpenClusterEx</a> functions.


### -param lpszNodeName [in]

Pointer to the NetBIOS name of an existing node. If the DNS name of the node is used, the 
      <b>OpenClusterNode</b> function will fail and 
      <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
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
      <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-closeclusternode">CloseClusterNode</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusterex">OpenClusterEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusternodeex">OpenClusterNodeEx</a>
 

 

