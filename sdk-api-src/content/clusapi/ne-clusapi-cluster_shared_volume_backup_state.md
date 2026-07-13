---
UID: NE:clusapi._CLUSTER_SHARED_VOLUME_BACKUP_STATE
title: CLUSTER_SHARED_VOLUME_BACKUP_STATE (clusapi.h)
description: Describes the CSV backup state.
helpviewer_keywords: ["*PCLUSTER_SHARED_VOLUME_BACKUP_STATE","CLUSTER_SHARED_VOLUME_BACKUP_STATE","CLUSTER_SHARED_VOLUME_BACKUP_STATE enumeration [Failover Cluster]","PCLUSTER_SHARED_VOLUME_BACKUP_STATE","PCLUSTER_SHARED_VOLUME_BACKUP_STATE enumeration pointer [Failover Cluster]","VolumeBackupInProgress","VolumeBackupNone","clusapi/CLUSTER_SHARED_VOLUME_BACKUP_STATE","clusapi/PCLUSTER_SHARED_VOLUME_BACKUP_STATE","clusapi/VolumeBackupInProgress","clusapi/VolumeBackupNone","mscs.cluster_shared_volume_backup_state"]
old-location: mscs\cluster_shared_volume_backup_state.htm
tech.root: MsCS
ms.assetid: f83a7dfe-ad48-41e2-983e-75dfd921c137
ms.date: 12/05/2018
ms.keywords: '*PCLUSTER_SHARED_VOLUME_BACKUP_STATE, CLUSTER_SHARED_VOLUME_BACKUP_STATE, CLUSTER_SHARED_VOLUME_BACKUP_STATE enumeration [Failover Cluster], PCLUSTER_SHARED_VOLUME_BACKUP_STATE, PCLUSTER_SHARED_VOLUME_BACKUP_STATE enumeration pointer [Failover Cluster], VolumeBackupInProgress, VolumeBackupNone, clusapi/CLUSTER_SHARED_VOLUME_BACKUP_STATE, clusapi/PCLUSTER_SHARED_VOLUME_BACKUP_STATE, clusapi/VolumeBackupInProgress, clusapi/VolumeBackupNone, mscs.cluster_shared_volume_backup_state'
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
req.typenames: CLUSTER_SHARED_VOLUME_BACKUP_STATE, *PCLUSTER_SHARED_VOLUME_BACKUP_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_SHARED_VOLUME_BACKUP_STATE
 - clusapi/_CLUSTER_SHARED_VOLUME_BACKUP_STATE
 - PCLUSTER_SHARED_VOLUME_BACKUP_STATE
 - clusapi/PCLUSTER_SHARED_VOLUME_BACKUP_STATE
 - CLUSTER_SHARED_VOLUME_BACKUP_STATE
 - clusapi/CLUSTER_SHARED_VOLUME_BACKUP_STATE
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
 - CLUSTER_SHARED_VOLUME_BACKUP_STATE
---

# CLUSTER_SHARED_VOLUME_BACKUP_STATE enumeration


## -description

Describes the cluster shared volume (CSV) backup state.

## -enum-fields

### -field VolumeBackupNone:0x00000000

There is no backup in progress for this CSV.

### -field VolumeBackupInProgress:0x00000001

There is a backup in progress for this CSV.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-set-shared-volume-backup-mode">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a>



<a href="/windows/desktop/api/clusapi/ns-clusapi-clus_shared_volume_backup_mode">CLUS_SHARED_VOLUME_BACKUP_MODE</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
