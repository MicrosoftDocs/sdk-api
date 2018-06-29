---
UID: NC:resapi.PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME
title: PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME
author: windows-sdk-content
description: Clears the backup state for the cluster shared volume.
old-location: mscs\clusterclearbackupstateforsharedvolume.htm
old-project: MsCS
ms.assetid: 54ebfff4-8898-49ed-9a45-07286cda5fb4
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME, PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME callback, PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME callback function [Failover Cluster], mscs.clusterclearbackupstateforsharedvolume, resapi/PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME callback function


## -description


Clears the backup state for the cluster shared volume (CSV). The <b>PCLUSTER_CLEAR_BACKUP_STATE_FOR_SHARED_VOLUME</b> type defines a pointer to this function.


## -parameters




### -param lpszVolumePathName [in]

Path to a file on a CSV. If the path is not a CSV path, 
      <i>ClusterClearBackupStateForSharedVolume</i> 
      will return <b>ERROR_INVALID_PARAMETER</b> (87).


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b> (0).

If the function fails, it returns one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



The 
    <i>ClusterClearBackupStateForSharedVolume</i> 
    function must be called from a node of the cluster.

Normally, when a backup job completes, the CSV "Backup in Progress" state (set by 
    <a href="https://msdn.microsoft.com/d30f1a5b-f231-4874-8e79-6d25cfd094a5">ClusterPrepareSharedVolumeForBackup</a>) 
    is automatically cleared—meaning that the CSV volume is unpinned from this Cluster node and 
    direct I/O is re-enabled. If the backup process is terminated after the call to 
    <i>ClusterPrepareSharedVolumeForBackup</i> 
    and before the snapshot creation process is complete, CSV will wait 30 minutes before it will clear the 
    "Backup in Progress" state. If the requester is able to safely determine that no other backups 
    are active on this CSV, 
    <i>ClusterClearBackupStateForSharedVolume</i> 
    may be called to clear the "Backup in Progress" state of the CSV volume.

<div class="alert"><b>Note</b>  When the 
     <i>ClusterClearBackupStateForSharedVolume</i> 
     function is called for a particular CSV volume, the Backup State for that CSV is cleared without regard to other 
     backups that could be active on any node within the Cluster. To avoid corruption of an in-progress backup, 
     extreme care must be taken to ensure that there are no other backups active for this CSV volume before 
     calling 
     <i>ClusterClearBackupStateForSharedVolume</i>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ea8b76b2-3931-4489-a648-e1077fd93b21">Backing Up and Restoring the Failover Cluster Configuration Using VSS</a>



<a href="https://msdn.microsoft.com/0f492e51-f364-40f1-b2c8-478f707f079d">Backup and Restore Functions</a>



<a href="https://msdn.microsoft.com/2ee69873-e562-4bac-bfed-119d56082095">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a>



<a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a>
 

 

