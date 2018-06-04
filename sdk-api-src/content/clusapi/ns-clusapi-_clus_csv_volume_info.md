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

# _CLUS_CSV_VOLUME_INFO structure


## -description


Represents information about a cluster shared volume (CSV). 


## -struct-fields




### -field VolumeOffset

The physical offset, in bytes, of the data on the CSV.


### -field PartitionNumber

The partition number of the CSV.


### -field FaultState

A <a href="https://msdn.microsoft.com/D3F065E5-3304-4B4E-BD85-04CAC050B001">CLUSTER_CSV_VOLUME_FAULT_STATE</a> enumeration value that specifies the fault state of the CSV.


### -field BackupState

A <a href="https://msdn.microsoft.com/f83a7dfe-ad48-41e2-983e-75dfd921c137">CLUSTER_SHARED_VOLUME_BACKUP_STATE</a> enumeration value that specifies the state of the CSV backup.


### -field szVolumeFriendlyName

The friendly name of the CSV.


### -field szVolumeName

The volume <b>GUID</b> path of the CSV.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

