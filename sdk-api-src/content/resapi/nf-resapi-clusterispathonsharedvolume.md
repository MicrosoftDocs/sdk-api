---
UID: NF:resapi.ClusterIsPathOnSharedVolume
title: ClusterIsPathOnSharedVolume function
author: windows-sdk-content
description: Determines whether a path is on a cluster shared volume.
old-location: mscs\clusterispathonsharedvolume.htm
tech.root: mscs
ms.assetid: 8d4702b8-23de-4c45-87ec-1a4ada8a4086
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ClusterIsPathOnSharedVolume, ClusterIsPathOnSharedVolume function [Failover Cluster], PCLUSTER_IS_PATH_ON_SHARED_VOLUME, PCLUSTER_IS_PATH_ON_SHARED_VOLUME function [Failover Cluster], mscs.clusterispathonsharedvolume, resapi/ClusterIsPathOnSharedVolume, resapi/PCLUSTER_IS_PATH_ON_SHARED_VOLUME
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Enterprise, Windows Server 2008 R2 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.Lib
req.dll: ResUtils.Dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.Dll
 - Ext-MS-Win-Cluster-Resutils-L1-1-1.dll
api_name:
 - ClusterIsPathOnSharedVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterIsPathOnSharedVolume function


## -description


Determines whether a path is on a cluster shared volume (CSV). This is used to determine whether <a href="https://msdn.microsoft.com/d110e30d-046e-45f3-b326-72160a69c17d">ClusterGetVolumeNameForVolumeMountPoint</a> or <a href="https://msdn.microsoft.com/eff2995a-d17c-4899-bff5-ead9526f859d">ClusterGetVolumePathName</a> should be called instead of <a href="https://msdn.microsoft.com/3f749042-bdc9-4087-bb8a-d833713472eb">GetVolumeNameForVolumeMountPoint</a> or <a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a>. The <b>PCLUSTER_IS_PATH_ON_SHARED_VOLUME</b> type defines a pointer to this function.


## -parameters




### -param lpszPathName [in]

A pointer to the input path string.


## -returns



<b>TRUE</b> if the path is on a CSV and this function is called from a domain account, or if the path is on a CSV that is owned by a local cluster node; otherwise, <b>FALSE</b>.




## -remarks



The 
    <b>ClusterIsPathOnSharedVolume</b> 
    function must be called from a node of the cluster.

The following table explains the possible return values based on the type of cluster node that owns the CSV and the type of user account that calls this function.

<table>
<tr>
<th></th>
<th colspan="2">User Account Type</th>
</tr>
<tr>
<th>CSV Ownership</th>
<td>Local</td>
<td>Domain</td>
</tr>
<tr>
<td>Local Cluster Node</td>
<td><b>TRUE</b></td>
<td><b>TRUE</b></td>
</tr>
<tr>
<td>Other Cluster Node</td>
<td><b>FALSE</b></td>
<td><b>TRUE</b></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ea8b76b2-3931-4489-a648-e1077fd93b21">Backing Up and Restoring the Failover Cluster Configuration Using VSS</a>



<a href="https://msdn.microsoft.com/0f492e51-f364-40f1-b2c8-478f707f079d">Backup and Restore Functions</a>



<a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a>
 

 

