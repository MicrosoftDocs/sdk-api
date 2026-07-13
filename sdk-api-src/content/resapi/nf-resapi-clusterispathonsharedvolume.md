---
UID: NF:resapi.ClusterIsPathOnSharedVolume
title: ClusterIsPathOnSharedVolume function (resapi.h)
description: Determines whether a path is on a cluster shared volume.
helpviewer_keywords: ["ClusterIsPathOnSharedVolume","ClusterIsPathOnSharedVolume function [Failover Cluster]","PCLUSTER_IS_PATH_ON_SHARED_VOLUME","PCLUSTER_IS_PATH_ON_SHARED_VOLUME function [Failover Cluster]","mscs.clusterispathonsharedvolume","resapi/ClusterIsPathOnSharedVolume","resapi/PCLUSTER_IS_PATH_ON_SHARED_VOLUME"]
old-location: mscs\clusterispathonsharedvolume.htm
tech.root: MsCS
ms.assetid: 8d4702b8-23de-4c45-87ec-1a4ada8a4086
ms.date: 12/05/2018
ms.keywords: ClusterIsPathOnSharedVolume, ClusterIsPathOnSharedVolume function [Failover Cluster], PCLUSTER_IS_PATH_ON_SHARED_VOLUME, PCLUSTER_IS_PATH_ON_SHARED_VOLUME function [Failover Cluster], mscs.clusterispathonsharedvolume, resapi/ClusterIsPathOnSharedVolume, resapi/PCLUSTER_IS_PATH_ON_SHARED_VOLUME
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterIsPathOnSharedVolume
 - resapi/ClusterIsPathOnSharedVolume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ext-ms-win-cluster-resutils-l1-1-2.dll
 - ResUtils.Dll
 - Ext-MS-Win-Cluster-Resutils-L1-1-1.dll
api_name:
 - ClusterIsPathOnSharedVolume
---

# ClusterIsPathOnSharedVolume function


## -description

Determines whether a path is on a cluster shared volume (CSV). This is used to determine whether <a href="/windows/desktop/api/resapi/nf-resapi-clustergetvolumenameforvolumemountpoint">ClusterGetVolumeNameForVolumeMountPoint</a> or <a href="/windows/desktop/api/resapi/nf-resapi-clustergetvolumepathname">ClusterGetVolumePathName</a> should be called instead of <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a> or <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumepathnamew">GetVolumePathName</a>. The <b>PCLUSTER_IS_PATH_ON_SHARED_VOLUME</b> type defines a pointer to this function.

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

<a href="/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss">Backing Up and Restoring the Failover Cluster Configuration Using VSS</a>



<a href="/previous-versions/windows/desktop/mscs/backup-and-restore-functions">Backup and Restore Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumepathnamew">GetVolumePathName</a>