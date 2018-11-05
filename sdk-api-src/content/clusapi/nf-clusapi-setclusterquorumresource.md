---
UID: NF:clusapi.SetClusterQuorumResource
title: SetClusterQuorumResource function
author: windows-sdk-content
description: Establishes a resource as the quorum resource for a cluster.
old-location: mscs\setclusterquorumresource.htm
tech.root: mscs
ms.assetid: 1a00c09e-4470-4c02-807d-c559fd992066
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CLUS_HYBRID_QUORUM, CLUS_LEGACY_QUORUM, CLUS_NODE_MAJORITY_QUORUM, PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE, PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE function [Failover Cluster], SetClusterQuorumResource, SetClusterQuorumResource function [Failover Cluster], _wolf_setclusterquorumresource, clusapi/PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE, clusapi/SetClusterQuorumResource, mscs.setclusterquorumresource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
api_name:
 - SetClusterQuorumResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClusterQuorumResource function


## -description


Establishes a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> as the 
    <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a> for a 
    <a href="c_gly.htm">cluster</a>. The <b>PCLUSAPI_SET_CLUSTER_QUORUM_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the new quorum resource; or the existing 
       <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a> when 
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
The <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> uses the partition flagged as 
       <b>CLUSPROP_PIFLAG_DEFAULT_QUORUM</b> as the default partition (see 
       <a href="https://msdn.microsoft.com/cda1e334-dba8-4fe9-b035-4e475245869c">CLUSPROP_PARTITION_INFO</a>), or, if the flag 
       cannot be found, the first available NTFS partition on the new quorum resource.

For the default path name, the Cluster service uses the previous path name if one exists; otherwise it uses 
       "MSCS".


### -param dwMaxQuoLogSize [in]

The quorum type value. Specify one of the three constants listed. When you specify <b>CLUS_NODE_MAJORITY_QUORUM</b>, <i> hResource</i> must refer to the existing <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a>.



#### CLUS_HYBRID_QUORUM (1024 (0x400))



#### CLUS_NODE_MAJORITY_QUORUM (0 (0x0))



#### CLUS_LEGACY_QUORUM (4194304 (0x400000))


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error 
       code.




## -remarks



Do not call <b>SetClusterQuorumResource</b> from 
     a resource DLL. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f841070-9dc0-49e0-9112-8d46185470b5">GetClusterQuorumResource</a>
 

 

