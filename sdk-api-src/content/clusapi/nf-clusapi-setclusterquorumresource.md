---
UID: NF:clusapi.SetClusterQuorumResource
title: SetClusterQuorumResource function (clusapi.h)
description: Establishes a resource as the quorum resource for a cluster.
helpviewer_keywords: ["CLUS_HYBRID_QUORUM","CLUS_LEGACY_QUORUM","CLUS_NODE_MAJORITY_QUORUM","PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE","PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE function [Failover Cluster]","SetClusterQuorumResource","SetClusterQuorumResource function [Failover Cluster]","_wolf_setclusterquorumresource","clusapi/PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE","clusapi/SetClusterQuorumResource","mscs.setclusterquorumresource"]
old-location: mscs\setclusterquorumresource.htm
tech.root: MsCS
ms.assetid: 1a00c09e-4470-4c02-807d-c559fd992066
ms.date: 12/05/2018
ms.keywords: CLUS_HYBRID_QUORUM, CLUS_LEGACY_QUORUM, CLUS_NODE_MAJORITY_QUORUM, PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE, PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE function [Failover Cluster], SetClusterQuorumResource, SetClusterQuorumResource function [Failover Cluster], _wolf_setclusterquorumresource, clusapi/PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE, clusapi/SetClusterQuorumResource, mscs.setclusterquorumresource
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
 - SetClusterQuorumResource
 - clusapi/SetClusterQuorumResource
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
 - SetClusterQuorumResource
---

# SetClusterQuorumResource function


## -description

Establishes a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> as the 
    <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a> for a 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. The <b>PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the new quorum resource; or the existing 
       <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a> when 
       <i>dwMaxQuoLogSize</i> is 
       <b>CLUS_NODE_MAJORITY_QUORUM</b>.

### -param lpszDeviceName [in, optional]

Determines the drive letter and path that the Cluster service will use to maintain the quorum files on the 
       new quorum resource. Pass a null-terminated Unicode string or <b>NULL</b>, as follows.

<ul>
<li>If you specify a drive letter in the path, the Cluster service will verify that the drive letter refers 
        to a valid partition on the new quorum resource.</li>
<li>If you do not specify a drive letter in the path, the Cluster service will use a default partition on the 
        new quorum resource (see below).</li>
<li>If <b>NULL</b>, the Cluster service will use a default partition and a default path 
        name (see below).</li>
</ul>
The <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> uses the partition flagged as 
       <b>CLUSPROP_PIFLAG_DEFAULT_QUORUM</b> as the default partition (see 
       <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a>), or, if the flag 
       cannot be found, the first available NTFS partition on the new quorum resource.

For the default path name, the Cluster service uses the previous path name if one exists; otherwise it uses 
       "MSCS".

### -param dwMaxQuoLogSize [in]

The quorum type value. Specify one of the three constants listed. When you specify <b>CLUS_NODE_MAJORITY_QUORUM</b>, <i> hResource</i> must refer to the existing <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a>.



#### CLUS_HYBRID_QUORUM (1024 (0x400))



#### CLUS_NODE_MAJORITY_QUORUM (0 (0x0))



#### CLUS_LEGACY_QUORUM (4194304 (0x400000))

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error 
       code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_NOT_ONLINE</b></dt>
<dt>5004 (0x138C)</dt>
</dl>
</td>
<td width="60%">
The quorum resource is not online.

</td>
</tr>
</table>

## -remarks

Do not call <b>SetClusterQuorumResource</b> from 
     a resource DLL. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterquorumresource">GetClusterQuorumResource</a>