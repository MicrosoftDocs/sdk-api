---
UID: NF:resapi.ClusterClearBackupStateForSharedVolume
title: ClusterClearBackupStateForSharedVolume function
author: windows-sdk-content
description: Clears the backup state for the cluster shared volume.
old-location: mscs\clusterclearbackupstateforsharedvolume.htm
tech.root: mscs
ms.assetid: 54ebfff4-8898-49ed-9a45-07286cda5fb4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterClearBackupStateForSharedVolume, ClusterClearBackupStateForSharedVolume function [Failover Cluster], PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME, PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME function [Failover Cluster], mscs.clusterclearbackupstateforsharedvolume, resapi/ClusterClearBackupStateForSharedVolume, resapi/PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME
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
api_name:
 - ClusterClearBackupStateForSharedVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterClearBackupStateForSharedVolume function


## -description


Clears the backup state for the cluster shared volume (CSV). The <b>PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME</b> type defines a pointer to this function.


## -parameters




### -param lpszVolumePathName [in]

Path to a file on a CSV. If the path is not a CSV path, 
      <b>ClusterClearBackupStateForSharedVolume</b> 
      will return <b>ERROR_INVALID_PARAMETER</b> (87).


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b> (0).

If the function fails, it returns one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



The 
    <b>ClusterClearBackupStateForSharedVolume</b> 
    function must be called from a node of the cluster.

Normally, when a backup job completes, the CSV "Backup in Progress" state (set by 
    <a href="https://msdn.microsoft.com/d30f1a5b-f231-4874-8e79-6d25cfd094a5">ClusterPrepareSharedVolumeForBackup</a>) 
    is automatically cleared—meaning that the CSV volume is unpinned from this Cluster node and 
    direct I/O is re-enabled. If the backup process is terminated after the call to 
    <b>ClusterPrepareSharedVolumeForBackup</b> 
    and before the snapshot creation process is complete, CSV will wait 30 minutes before it will clear the 
    "Backup in Progress" state. If the requester is able to safely determine that no other backups 
    are active on this CSV, 
    <b>ClusterClearBackupStateForSharedVolume</b> 
    may be called to clear the "Backup in Progress" state of the CSV volume.

<div class="alert"><b>Note</b>  When the 
     <b>ClusterClearBackupStateForSharedVolume</b> 
     function is called for a particular CSV volume, the Backup State for that CSV is cleared without regard to other 
     backups that could be active on any node within the Cluster. To avoid corruption of an in-progress backup, 
     extreme care must be taken to ensure that there are no other backups active for this CSV volume before 
     calling 
     <b>ClusterClearBackupStateForSharedVolume</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ea8b76b2-3931-4489-a648-e1077fd93b21">Backing Up and Restoring the Failover Cluster Configuration Using VSS</a>



<a href="https://msdn.microsoft.com/0f492e51-f364-40f1-b2c8-478f707f079d">Backup and Restore Functions</a>



<a href="https://msdn.microsoft.com/2ee69873-e562-4bac-bfed-119d56082095">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a>



<a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a>
 

 

