---
UID: NF:clusapi.GetClusterNetworkId
title: GetClusterNetworkId function (clusapi.h)
description: Returns the identifier of a network.
helpviewer_keywords: ["GetClusterNetworkId","GetClusterNetworkId function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_NETWORK_ID","PCLUSAPI_GET_CLUSTER_NETWORK_ID function [Failover Cluster]","_wolf_getclusternetworkid","clusapi/GetClusterNetworkId","clusapi/PCLUSAPI_GET_CLUSTER_NETWORK_ID","mscs.getclusternetworkid"]
old-location: mscs\getclusternetworkid.htm
tech.root: MsCS
ms.assetid: 25091883-12fa-41b6-9ac0-70bc22db3f05
ms.date: 12/05/2018
ms.keywords: GetClusterNetworkId, GetClusterNetworkId function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NETWORK_ID, PCLUSAPI_GET_CLUSTER_NETWORK_ID function [Failover Cluster], _wolf_getclusternetworkid, clusapi/GetClusterNetworkId, clusapi/PCLUSAPI_GET_CLUSTER_NETWORK_ID, mscs.getclusternetworkid
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
 - GetClusterNetworkId
 - clusapi/GetClusterNetworkId
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
 - GetClusterNetworkId
---

# GetClusterNetworkId function


## -description

Returns the identifier of a  <a href="/previous-versions/windows/desktop/mscs/networks">network</a>. The <b>PCLUSAPI_GET_CLUSTER_NETWORK_ID</b> type defines a pointer to this function.

## -parameters

### -param hNetwork [in]

Handle to a network.

### -param lpszNetworkId [out]

Pointer to the identifier of the network associated with <i>hNetwork</i>, including the null-terminating character.

### -param lpcchName [in, out]

Pointer to the size of the <i>lpszNetworkID</i> buffer as a count of characters. On input, specify the maximum number of characters the buffer can hold, including the terminating <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding the terminating <b>NULL</b>.

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
The buffer pointed to by <i>lpszNetworkID</i> is not big enough to hold the result. The <i>lpcchNetworkID</i> parameter returns the number of characters in the result, excluding the terminating <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Note that <i>lpcchNetworkID</i> refers to a count of characters and not a count of bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing buffers, see  <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetwork">OpenClusterNetwork</a>