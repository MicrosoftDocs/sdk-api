---
UID: NF:clusapi.GetClusterNetInterface
title: GetClusterNetInterface function (clusapi.h)
description: Returns the name of a node's interface to a network in a cluster.
helpviewer_keywords: ["GetClusterNetInterface","GetClusterNetInterface function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_NET_INTERFACE","PCLUSAPI_GET_CLUSTER_NET_INTERFACE function [Failover Cluster]","_wolf_getclusternetinterface","clusapi/GetClusterNetInterface","clusapi/PCLUSAPI_GET_CLUSTER_NET_INTERFACE","mscs.getclusternetinterface"]
old-location: mscs\getclusternetinterface.htm
tech.root: MsCS
ms.assetid: b9bca010-7401-4a2f-95df-a5d0ef3dbfae
ms.date: 12/05/2018
ms.keywords: GetClusterNetInterface, GetClusterNetInterface function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NET_INTERFACE, PCLUSAPI_GET_CLUSTER_NET_INTERFACE function [Failover Cluster], _wolf_getclusternetinterface, clusapi/GetClusterNetInterface, clusapi/PCLUSAPI_GET_CLUSTER_NET_INTERFACE, mscs.getclusternetinterface
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
 - GetClusterNetInterface
 - clusapi/GetClusterNetInterface
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
 - GetClusterNetInterface
---

# GetClusterNetInterface function


## -description

Returns the name of a  <a href="/previous-versions/windows/desktop/mscs/nodes">node's</a> interface to a  <a href="/previous-versions/windows/desktop/mscs/networks">network</a> in a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. The <b>PCLUSAPI_GET_CLUSTER_NET_INTERFACE</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to a cluster.

### -param lpszNodeName [in]

Pointer to a null-terminated Unicode string containing the name of the node in the cluster.

### -param lpszNetworkName [in]

Pointer to a null-terminated Unicode string containing the name of the network.

### -param lpszInterfaceName [out]

Pointer to an output buffer holding the name of the  <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>.

### -param lpcchInterfaceName [in, out]

Pointer to the size of the <i>lpszInterfaceName</i> buffer as a count of characters. On input, specify the maximum number of characters the buffer can hold, including the terminating <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding the terminating <b>NULL</b>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is one of the possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpszInterfaceName</i> is not big enough to hold the result. The <i>lpcchInterfaceName</i> parameter returns the number of characters in the result, excluding the terminating <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Note that <i>lpcchInterfaceName</i> refers to a count of characters and not a count of bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing buffers, see  <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>