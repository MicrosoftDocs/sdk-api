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

# _CLUS_SHARED_VOLUME_BACKUP_MODE structure


## -description


Describes the backup mode for cluster shared volume (CSV). Used by the 
    <a href="https://msdn.microsoft.com/2ee69873-e562-4bac-bfed-119d56082095">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a> <a href="https://msdn.microsoft.com/b8ab57bd-f83e-46c2-9c9c-02107c3881bf">control code</a>.


## -struct-fields




### -field BackupState


Value from 
       <a href="https://msdn.microsoft.com/f83a7dfe-ad48-41e2-983e-75dfd921c137">CLUSTER_SHARED_VOLUME_BACKUP_STATE</a> 
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




<a href="https://msdn.microsoft.com/2ee69873-e562-4bac-bfed-119d56082095">CLUSCTL_RESOURCE_SET_SHARED_VOLUME_BACKUP_MODE</a>



<a href="https://msdn.microsoft.com/f83a7dfe-ad48-41e2-983e-75dfd921c137">CLUSTER_SHARED_VOLUME_BACKUP_STATE</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

