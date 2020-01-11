---
UID: NF:clusapi.CloseClusterNode
title: CloseClusterNode function (clusapi.h)
description: Closes a node handle.
old-location: mscs\closeclusternode.htm
tech.root: MsCS
ms.assetid: e2d90b7e-d181-48b6-a891-b885c24a15ea
ms.date: 12/05/2018
ms.keywords: CloseClusterNode, CloseClusterNode function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_NODE, PCLUSAPI_CLOSE_CLUSTER_NODE function [Failover Cluster], _wolf_closeclusternode, clusapi/CloseClusterNode, clusapi/PCLUSAPI_CLOSE_CLUSTER_NODE, mscs.closeclusternode
f1_keywords:
- clusapi/CloseClusterNode
dev_langs:
- c++
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
- ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
- CloseClusterNode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseClusterNode function


## -description


Closes a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a> handle. The <b>PCLUSAPI_CLOSE_CLUSTER_NODE</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to an existing node.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function  <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>
 

 

