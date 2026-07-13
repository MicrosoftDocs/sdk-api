---
UID: NF:clusapi.OpenClusterNetwork
title: OpenClusterNetwork function (clusapi.h)
description: Opens a connection to a network and returns a handle to it. (OpenClusterNetwork)
helpviewer_keywords: ["OpenClusterNetwork","OpenClusterNetwork function [Failover Cluster]","PCLUSAPI_OPEN_CLUSTER_NETWORK","PCLUSAPI_OPEN_CLUSTER_NETWORK function [Failover Cluster]","_wolf_openclusternetwork","clusapi/OpenClusterNetwork","clusapi/PCLUSAPI_OPEN_CLUSTER_NETWORK","mscs.openclusternetwork"]
old-location: mscs\openclusternetwork.htm
tech.root: MsCS
ms.assetid: a888ca91-e56f-42bc-81c5-9235c6fd5172
ms.date: 12/05/2018
ms.keywords: OpenClusterNetwork, OpenClusterNetwork function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER_NETWORK, PCLUSAPI_OPEN_CLUSTER_NETWORK function [Failover Cluster], _wolf_openclusternetwork, clusapi/OpenClusterNetwork, clusapi/PCLUSAPI_OPEN_CLUSTER_NETWORK, mscs.openclusternetwork
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
 - OpenClusterNetwork
 - clusapi/OpenClusterNetwork
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
 - OpenClusterNetwork
---

# OpenClusterNetwork function


## -description

Opens a connection to a <a href="/previous-versions/windows/desktop/mscs/networks">network</a> and returns a handle 
    to it. The <b>PCLUSAPI_OPEN_CLUSTER_NETWORK</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

### -param lpszNetworkName [in]

Pointer to the name of an existing network.

## -returns

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
 

If the operation was successful, 
       <b>OpenClusterNetwork</b> returns a network handle.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusternetwork">CloseClusterNetwork</a>



<a href="/previous-versions/windows/desktop/mscs/network-management-functions">Failover Cluster Network Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetworkex">OpenClusterNetworkEx</a>
