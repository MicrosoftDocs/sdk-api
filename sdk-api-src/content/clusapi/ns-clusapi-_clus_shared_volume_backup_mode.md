---
UID: NS:clusapi._CLUS_SHARED_VOLUME_BACKUP_MODE
title: "_CLUS_SHARED_VOLUME_BACKUP_MODE"
author: windows-sdk-content
description: Describes the backup mode for CSV.
old-location: mscs\clus_shared_volume_backup_mode.htm
tech.root: MsCS
ms.assetid: e5ae8cc7-bff8-4293-920e-3a704d1bd7e5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PCLUS_SHARED_VOLUME_BACKUP_MODE, CLUS_SHARED_VOLUME_BACKUP_MODE, CLUS_SHARED_VOLUME_BACKUP_MODE structure [Failover Cluster], PCLUS_SHARED_VOLUME_BACKUP_MODE, PCLUS_SHARED_VOLUME_BACKUP_MODE structure pointer [Failover Cluster], VolumeBackupInProgress, VolumeBackupNone, _CLUS_SHARED_VOLUME_BACKUP_MODE, clusapi/CLUS_SHARED_VOLUME_BACKUP_MODE, clusapi/PCLUS_SHARED_VOLUME_BACKUP_MODE, mscs.clus_shared_volume_backup_mode"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - CLUS_SHARED_VOLUME_BACKUP_MODE
product: Windows
targetos: Windows
req.typenames: CLUS_SHARED_VOLUME_BACKUP_MODE, *PCLUS_SHARED_VOLUME_BACKUP_MODE
req.redist: 
---

# _CLUS_SHARED_VOLUME_BACKUP_MODE structure


## -description


Describes the backup mode for cluster shared volume (CSV). Used by the 
    <a href="https://msdn.microsoft.com/en-us/library/Ee342498(v=VS.85).aspx">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a> <a href="https://msdn.microsoft.com/en-us/library/Aa367127(v=VS.85).aspx">control code</a>.


## -struct-fields




### -field BackupState


Value from 
       <a href="https://msdn.microsoft.com/en-us/library/Ee342508(v=VS.85).aspx">CLUSTER_SHARED_VOLUME_BACKUP_STATE</a> 
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




<a href="https://msdn.microsoft.com/en-us/library/Ee342498(v=VS.85).aspx">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee342508(v=VS.85).aspx">CLUSTER_SHARED_VOLUME_BACKUP_STATE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data Structures</a>
 

 

