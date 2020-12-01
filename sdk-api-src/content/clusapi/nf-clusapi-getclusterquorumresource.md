---
UID: NF:clusapi.GetClusterQuorumResource
title: GetClusterQuorumResource function (clusapi.h)
description: Returns the name of a cluster's quorum resource.
helpviewer_keywords: ["GetClusterQuorumResource","GetClusterQuorumResource function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_QUORUM_RESOURCE","PCLUSAPI_GET_CLUSTER_QUORUM_RESOURCE function [Failover Cluster]","_wolf_getclusterquorumresource","clusapi/GetClusterQuorumResource","clusapi/PCLUSAPI_GET_CLUSTER_QUORUM_RESOURCE","mscs.getclusterquorumresource"]
old-location: mscs\getclusterquorumresource.htm
tech.root: MsCS
ms.assetid: 0f841070-9dc0-49e0-9112-8d46185470b5
ms.date: 12/05/2018
ms.keywords: GetClusterQuorumResource, GetClusterQuorumResource function [Failover Cluster], PCLUSAPI_GET_CLUSTER_QUORUM_RESOURCE, PCLUSAPI_GET_CLUSTER_QUORUM_RESOURCE function [Failover Cluster], _wolf_getclusterquorumresource, clusapi/GetClusterQuorumResource, clusapi/PCLUSAPI_GET_CLUSTER_QUORUM_RESOURCE, mscs.getclusterquorumresource
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
 - GetClusterQuorumResource
 - clusapi/GetClusterQuorumResource
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
 - GetClusterQuorumResource
---

# GetClusterQuorumResource function


## -description

Returns the name of a cluster's  <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a>. The <b>PCLUSAPI_GET_CLUSTER_QUORUM_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to an existing <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

### -param lpszResourceName [out]

Pointer to a null-terminated Unicode string containing the name of the cluster's quorum resource. The name is read from the quorum resource's  <a href="/previous-versions/windows/desktop/mscs/resources-name">Name</a> common property. Do not pass <b>NULL</b> for this parameter.

### -param lpcchResourceName [in, out]

Pointer to the size of the <i>lpszResourceName</i> buffer as a count of characters. On input, specify the maximum number of characters the buffer can hold, including the terminating <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding the terminating <b>NULL</b>.

### -param lpszDeviceName [out]

Pointer to a null-terminated Unicode string containing the path to the location of the quorum log files maintained by the  <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>. Do not pass <b>NULL</b> for this parameter.

### -param lpcchDeviceName [in, out]

Pointer to the size of the <i>lpszDeviceName</i> buffer as a count of characters. On input, specify the maximum number of characters the buffer can hold, including the terminating <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding the terminating <b>NULL</b>.

### -param lpdwMaxQuorumLogSize [out]

Pointer to the maximum size (in bytes) of the log being maintained by the quorum resource. Do not pass <b>NULL</b> for this parameter.

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
The <i>lpszResourceName</i> or the <i>lpszDeviceName</i> buffer is not big enough to hold the result. The <i>lpcchResourceName</i> and <i>lpcchDeviceName</i> parameters return the number of characters in the result, excluding the terminating <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing buffers, see  <a href="/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resources-name">Name</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-setclusterquorumresource">SetClusterQuorumResource</a>