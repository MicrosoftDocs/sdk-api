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

# CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE enumeration


## -description


Specifies the various snapshot states for a shared volume.


## -enum-fields




### -field ClusterSharedVolumeSnapshotStateUnknown

Indicates that the snapshot state is unknow.


### -field ClusterSharedVolumePrepareForHWSnapshot

Indicates that the snapshot is being created.


### -field ClusterSharedVolumeHWSnapshotCompleted

Indicates that the snapshot is completed.


### -field ClusterSharedVolumePrepareForFreeze

TBD


## -see-also




<a href="https://msdn.microsoft.com/B264CF0E-33FD-44F9-B91E-2F90C35D09AC">ClusterSharedVolumeSetSnapshotState</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

