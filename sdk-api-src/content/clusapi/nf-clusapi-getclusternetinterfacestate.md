---
UID: NF:clusapi.GetClusterNetInterfaceState
title: GetClusterNetInterfaceState function (clusapi.h)
description: Returns the current state of a network interface.
helpviewer_keywords: ["GetClusterNetInterfaceState","GetClusterNetInterfaceState function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE","PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE function [Failover Cluster]","_wolf_getclusternetinterfacestate","clusapi/GetClusterNetInterfaceState","clusapi/PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE","mscs.getclusternetinterfacestate"]
old-location: mscs\getclusternetinterfacestate.htm
tech.root: MsCS
ms.assetid: d84a5e3f-d0f9-4345-b008-e15c277dcbd5
ms.date: 12/05/2018
ms.keywords: GetClusterNetInterfaceState, GetClusterNetInterfaceState function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE, PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE function [Failover Cluster], _wolf_getclusternetinterfacestate, clusapi/GetClusterNetInterfaceState, clusapi/PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE, mscs.getclusternetinterfacestate
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
 - GetClusterNetInterfaceState
 - clusapi/GetClusterNetInterfaceState
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
 - GetClusterNetInterfaceState
---

# GetClusterNetInterfaceState function


## -description

Returns the current state of a 
    <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>. The <b>PCLUSAPI_GET_CLUSTER_NET_INTERFACE_STATE</b> type defines a pointer to this function.

## -parameters

### -param hNetInterface [in]

Handle to the network interface for which state information should be returned.

## -returns

<b>GetClusterNetInterfaceState</b> returns 
       the current state of the network interface, which is represented by one of the following values enumerated by 
       the <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_netinterface_state">CLUSTER_NETINTERFACE_STATE</a> 
       enumeration.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetInterfaceFailed</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The network interface cannot communicate with any other network interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetInterfaceUnreachable</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The network interface cannot communicate with at least one other network interface whose state is not <b>ClusterNetInterfaceFailed</b> or <b>ClusterNetInterfaceUnavailable</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetInterfaceUp</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The network interface can communicate with all other network interfaces whose state is not <b>ClusterNetInterfaceFailed</b> or <b>ClusterNetInterfaceUnavailable</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetInterfaceUnavailable</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The node that owns the network interface is down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetInterfaceStateUnknown</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_netinterface_state">CLUSTER_NETINTERFACE_STATE</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetinterface">OpenClusterNetInterface</a>



<a href="/previous-versions/windows/desktop/mscs/clusnetinterface-state">State Property of the ClusNetInterface Object</a>