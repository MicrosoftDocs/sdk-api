---
UID: NS:clusapi._CLUS_SHARED_VOLUME_BACKUP_MODE
title: CLUS_SHARED_VOLUME_BACKUP_MODE (clusapi.h)
description: Describes the backup mode for CSV.
helpviewer_keywords: ["*PCLUS_SHARED_VOLUME_BACKUP_MODE","CLUS_SHARED_VOLUME_BACKUP_MODE","CLUS_SHARED_VOLUME_BACKUP_MODE structure [Failover Cluster]","PCLUS_SHARED_VOLUME_BACKUP_MODE","PCLUS_SHARED_VOLUME_BACKUP_MODE structure pointer [Failover Cluster]","VolumeBackupInProgress","VolumeBackupNone","clusapi/CLUS_SHARED_VOLUME_BACKUP_MODE","clusapi/PCLUS_SHARED_VOLUME_BACKUP_MODE","mscs.clus_shared_volume_backup_mode"]
old-location: mscs\clus_shared_volume_backup_mode.htm
tech.root: MsCS
ms.assetid: e5ae8cc7-bff8-4293-920e-3a704d1bd7e5
ms.date: 12/05/2018
ms.keywords: '*PCLUS_SHARED_VOLUME_BACKUP_MODE, CLUS_SHARED_VOLUME_BACKUP_MODE, CLUS_SHARED_VOLUME_BACKUP_MODE structure [Failover Cluster], PCLUS_SHARED_VOLUME_BACKUP_MODE, PCLUS_SHARED_VOLUME_BACKUP_MODE structure pointer [Failover Cluster], VolumeBackupInProgress, VolumeBackupNone, clusapi/CLUS_SHARED_VOLUME_BACKUP_MODE, clusapi/PCLUS_SHARED_VOLUME_BACKUP_MODE, mscs.clus_shared_volume_backup_mode'
req.header: clusapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CLUS_SHARED_VOLUME_BACKUP_MODE, *PCLUS_SHARED_VOLUME_BACKUP_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUS_SHARED_VOLUME_BACKUP_MODE
 - clusapi/_CLUS_SHARED_VOLUME_BACKUP_MODE
 - PCLUS_SHARED_VOLUME_BACKUP_MODE
 - clusapi/PCLUS_SHARED_VOLUME_BACKUP_MODE
 - CLUS_SHARED_VOLUME_BACKUP_MODE
 - clusapi/CLUS_SHARED_VOLUME_BACKUP_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_SHARED_VOLUME_BACKUP_MODE
---

# CLUS_SHARED_VOLUME_BACKUP_MODE structure


## -description

Describes the backup mode for cluster shared volume (CSV). Used by the 
    <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-set-shared-volume-backup-mode">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a> <a href="/previous-versions/windows/desktop/mscs/about-control-codes">control code</a>.

## -struct-fields

### -field BackupState

Value from 
       <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_shared_volume_backup_state">CLUSTER_SHARED_VOLUME_BACKUP_STATE</a> 
       enumeration.





#### VolumeBackupNone (0)

There is no backup in progress for this CSV.



#### VolumeBackupInProgress (1)

There is a backup in progress for this CSV.

### -field DelayTimerInSecs

If the <b>BackupState</b> member is set to <b>VolumeBackupNone</b> 
      then this member must be set to 0. Otherwise this member must be set to a nonzero value.

### -field VolumeName

Null-terminated Unicode string containing the name of the shared volume. The name provided can 
      be either the cluster-assigned friendly name or the volume GUID path of the form 
      "\\?\Volume{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}\".

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-set-shared-volume-backup-mode">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a>



<a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_shared_volume_backup_state">CLUSTER_SHARED_VOLUME_BACKUP_STATE</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>