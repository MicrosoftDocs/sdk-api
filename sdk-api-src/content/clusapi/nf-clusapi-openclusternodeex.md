---
UID: NF:clusapi.OpenClusterNodeEx
title: OpenClusterNodeEx function (clusapi.h)
description: Opens a node and returns a handle to it. (OpenClusterNodeEx)
helpviewer_keywords: ["OpenClusterNodeEx","OpenClusterNodeEx function [Failover Cluster]","PCLUSAPI_OPEN_CLUSTER_NODE_EX","PCLUSAPI_OPEN_CLUSTER_NODE_EX function [Failover Cluster]","clusapi/OpenClusterNodeEx","clusapi/PCLUSAPI_OPEN_CLUSTER_NODE_EX","mscs.openclusternodeex"]
old-location: mscs\openclusternodeex.htm
tech.root: MsCS
ms.assetid: 2db24a30-0e4e-4647-8975-c9f584c3a9da
ms.date: 12/05/2018
ms.keywords: OpenClusterNodeEx, OpenClusterNodeEx function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NODE_EX, PCLUSAPI_OPEN_CLUSTER_NODE_EX function [Failover Cluster], clusapi/OpenClusterNodeEx, clusapi/PCLUSAPI_OPEN_CLUSTER_NODE_EX, mscs.openclusternodeex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
 - OpenClusterNodeEx
 - clusapi/OpenClusterNodeEx
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
 - OpenClusterNodeEx
---

# OpenClusterNodeEx function


## -description

Opens a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> and returns a handle to it.

## -parameters

### -param hCluster [in]

Handle to a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> returned from the 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a> or 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterex">OpenClusterEx</a> functions.

### -param lpszNodeName [in, optional]

Pointer to the NetBIOS name of an existing node. If the DNS name of the node is used, the 
      <b>OpenClusterNodeEx</b> function will fail and 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
      <b>ERROR_CLUSTER_NODE_NOT_FOUND</b>.

### -param dwDesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>.

### -param lpdwGrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.

## -returns

If the operation was successful, 
      <b>OpenClusterNodeEx</b> returns a node handle.

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
The operation was not successful. For more information about the error, call the 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. If the target server does not 
        support the <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternodeex">OpenClusterNodeEx</a> function (for 
        example if the target server is running Windows Server 2008 or earlier) then the 
        <b>GetLastError</b> function will return 
        <b>RPC_S_PROCNUM_OUT_OF_RANGE</b> (1745).

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusternode">CloseClusterNode</a>



<a href="/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterex">OpenClusterEx</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>
