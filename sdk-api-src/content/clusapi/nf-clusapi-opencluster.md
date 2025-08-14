---
UID: NF:clusapi.OpenCluster
title: OpenCluster function (clusapi.h)
description: Opens a connection to a cluster and returns a handle to it. (OpenCluster)
helpviewer_keywords: ["OpenCluster","OpenCluster function [Failover Cluster]","PCLUSAPI_OPEN_CLUSTER","PCLUSAPI_OPEN_CLUSTER function [Failover Cluster]","_wolf_opencluster","clusapi/OpenCluster","clusapi/PCLUSAPI_OPEN_CLUSTER","mscs.opencluster"]
old-location: mscs\opencluster.htm
tech.root: MsCS
ms.assetid: b2ee2575-cc1e-4696-8e95-9798fb556c58
ms.date: 12/05/2018
ms.keywords: OpenCluster, OpenCluster function [Failover Cluster], PCLUSAPI_OPEN_CLUSTER, PCLUSAPI_OPEN_CLUSTER function [Failover Cluster], _wolf_opencluster, clusapi/OpenCluster, clusapi/PCLUSAPI_OPEN_CLUSTER, mscs.opencluster
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
 - OpenCluster
 - clusapi/OpenCluster
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
 - OpenCluster
---

# OpenCluster function


## -description

Opens a connection to a 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and returns a handle to 
    it.

## -parameters

### -param lpszClusterName [in, optional]

Specifies one of the following values:

<ul>
<li>Pointer to a null-terminated Unicode string containing the name of the cluster or one of the cluster 
        <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> expressed as a NetBIOS name, a fully qualified DNS name, or 
        an IP address. This produces an RPC cluster handle.</li>
<li><b>NULL</b>, which produces an LPC handle to the cluster to which the local computer 
        belongs.</li>
</ul>

## -returns

If the operation was successful, <b>OpenCluster</b> returns 
       a cluster handle.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function 
         <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -remarks

A cluster handle is a pointer to an internally defined structure which stores information about the RPC or LPC 
     connection to the cluster. Any object handles obtained from the cluster handle will be associated with the RPC or 
     LPC session data stored in the cluster structure. Combining RPC and LPC handles or using handles obtained from 
     different contexts can cause exceptions or other unpredictable results. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/lpc-and-rpc-handles">LPC and RPC Handles</a>.

When finished with a cluster handle, it is important to call 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a> to ensure that all memory is freed and the 
     connection is shut down cleanly.

If the cluster is remote, the client must be running a compatible operating system. For example computers running 
     Windows Server 2008 cannot call <b>OpenCluster</b> against a 
     cluster running Windows Server 2016. To remotely manage these clusters, use 
     <a href="/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal">the Failover Cluster WMI Provider</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterex">OpenClusterEx</a>
