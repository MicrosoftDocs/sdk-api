---
UID: NF:resapi.ClusterPrepareSharedVolumeForBackup
title: ClusterPrepareSharedVolumeForBackup function (resapi.h)
description: ClusterPrepareSharedVolumeForBackup may be altered or unavailable.
helpviewer_keywords: ["ClusterPrepareSharedVolumeForBackup","ClusterPrepareSharedVolumeForBackup function [Failover Cluster]","PCLUSTER_PREPARE_SHARED_VOLUME_FOR_BACKUP","PCLUSTER_PREPARE_SHARED_VOLUME_FOR_BACKUP function [Failover Cluster]","mscs.clusterpreparesharedvolumeforbackup","resapi/ClusterPrepareSharedVolumeForBackup","resapi/PCLUSTER_PREPARE_SHARED_VOLUME_FOR_BACKUP"]
old-location: mscs\clusterpreparesharedvolumeforbackup.htm
tech.root: MsCS
ms.assetid: d30f1a5b-f231-4874-8e79-6d25cfd094a5
ms.date: 12/05/2018
ms.keywords: ClusterPrepareSharedVolumeForBackup, ClusterPrepareSharedVolumeForBackup function [Failover Cluster], PCLUSTER_PREPARE_SHARED_VOLUME_FOR_BACKUP, PCLUSTER_PREPARE_SHARED_VOLUME_FOR_BACKUP function [Failover Cluster], mscs.clusterpreparesharedvolumeforbackup, resapi/ClusterPrepareSharedVolumeForBackup, resapi/PCLUSTER_PREPARE_SHARED_VOLUME_FOR_BACKUP
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
 - ClusterPrepareSharedVolumeForBackup
 - resapi/ClusterPrepareSharedVolumeForBackup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.Dll
api_name:
 - ClusterPrepareSharedVolumeForBackup
---

# ClusterPrepareSharedVolumeForBackup function


## -description

<p class="CCE_Message">[<b>ClusterPrepareSharedVolumeForBackup</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

A call to this function is not required. The function does not do anything other than retrieve the volume path and the volume name.


<b>Windows Server 2008 R2:  </b>Prepares a cluster shared volume (CSV) for backup. This will mount the CSV locally, pin it to this cluster node, 
    disable direct I/O, and set the volume state to "Backup in Progress".

## -parameters

### -param lpszFileName [in]

Path to a directory or file on a cluster shared volume.

### -param lpszVolumePathName [out]

Address of buffer that will receive the CSV reparse point.

### -param lpcchVolumePathName [in, out]

Address of a <b>DWORD</b> that on input contains the size of the buffer (in 
      <b>WCHAR</b> characters) pointed to by the <i>lpszVolumePathName</i> 
      parameter and on output contains the size of the string written to that buffer. If size on input is not large 
      enough then the function will fail and return <b>ERROR_MORE_DATA</b> and set the 
      <b>DWORD</b> to the required size.

### -param lpszVolumeName [out]

Address of buffer that will receive the volume GUID path for the CSV.

### -param lpcchVolumeName [in, out]

Address of a <b>DWORD</b> that on input contains the size of the buffer (in 
      <b>WCHAR</b> characters) pointed to by the <i>lpszVolumeName</i> 
      parameter and on output contains the size of the string written to that buffer. If size on input is not large 
      enough then the function will fail and return <b>ERROR_MORE_DATA</b> and set the 
      <b>DWORD</b> to the required size.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

The 
    <b>ClusterPrepareSharedVolumeForBackup</b> 
    function must be called from a node of the cluster.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss">Backing Up and Restoring the Failover Cluster Configuration Using VSS</a>



<a href="/previous-versions/windows/desktop/mscs/backup-and-restore-functions">Backup and Restore Functions</a>