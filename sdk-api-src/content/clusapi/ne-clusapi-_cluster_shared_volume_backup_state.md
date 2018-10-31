---
UID: NE:clusapi._CLUSTER_SHARED_VOLUME_BACKUP_STATE
title: "_CLUSTER_SHARED_VOLUME_BACKUP_STATE"
author: windows-sdk-content
description: Describes the CSV backup state.
old-location: mscs\cluster_shared_volume_backup_state.htm
tech.root: mscs
ms.assetid: f83a7dfe-ad48-41e2-983e-75dfd921c137
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PCLUSTER_SHARED_VOLUME_BACKUP_STATE, CLUSTER_SHARED_VOLUME_BACKUP_STATE, CLUSTER_SHARED_VOLUME_BACKUP_STATE enumeration [Failover Cluster], PCLUSTER_SHARED_VOLUME_BACKUP_STATE, PCLUSTER_SHARED_VOLUME_BACKUP_STATE enumeration pointer [Failover Cluster], VolumeBackupInProgress, VolumeBackupNone, _CLUSTER_SHARED_VOLUME_BACKUP_STATE, clusapi/CLUSTER_SHARED_VOLUME_BACKUP_STATE, clusapi/PCLUSTER_SHARED_VOLUME_BACKUP_STATE, clusapi/VolumeBackupInProgress, clusapi/VolumeBackupNone, mscs.cluster_shared_volume_backup_state"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_SHARED_VOLUME_BACKUP_STATE
product: Windows
targetos: Windows
req.typenames: CLUSTER_SHARED_VOLUME_BACKUP_STATE, *PCLUSTER_SHARED_VOLUME_BACKUP_STATE
req.redist: 
---

# _CLUSTER_SHARED_VOLUME_BACKUP_STATE enumeration


## -description


Describes the cluster shared volume (CSV) backup state.


## -enum-fields




### -field VolumeBackupNone

There is no backup in progress for this CSV.


### -field VolumeBackupInProgress

There is a backup in progress for this CSV.


## -see-also




<a href="https://msdn.microsoft.com/2ee69873-e562-4bac-bfed-119d56082095">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a>



<a href="https://msdn.microsoft.com/e5ae8cc7-bff8-4293-920e-3a704d1bd7e5">CLUS_SHARED_VOLUME_BACKUP_MODE</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

