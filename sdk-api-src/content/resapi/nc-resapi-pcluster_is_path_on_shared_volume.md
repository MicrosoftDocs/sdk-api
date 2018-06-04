---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PCLUSTER_IS_PATH_ON_SHARED_VOLUME callback function


## -description


Determines whether a path is on a cluster shared volume (CSV). This is used to determine whether <a href="https://msdn.microsoft.com/d110e30d-046e-45f3-b326-72160a69c17d">ClusterGetVolumeNameForVolumeMountPoint</a> or <a href="https://msdn.microsoft.com/eff2995a-d17c-4899-bff5-ead9526f859d">ClusterGetVolumePathName</a> should be called instead of <a href="https://msdn.microsoft.com/3f749042-bdc9-4087-bb8a-d833713472eb">GetVolumeNameForVolumeMountPoint</a> or <a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a>. The <b>PCLUSTER_IS_PATH_ON_SHARED_VOLUME</b> type defines a pointer to this function.


## -parameters




### -param lpszPathName [in]

A pointer to the input path string.


## -returns



<b>TRUE</b> if the path is on a CSV and this function is called from a domain account, or if the path is on a CSV that is owned by a local cluster node; otherwise, <b>FALSE</b>.




## -remarks



The 
    <i>ClusterIsPathOnSharedVolume</i> 
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
 

 

