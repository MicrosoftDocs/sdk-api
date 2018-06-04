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

# _CLUSTER_CSV_VOLUME_FAULT_STATE enumeration


## -description


Defines the various fault states for a cluster shared volume (CSV).


## -enum-fields




### -field VolumeStateNoFaults

The CSV has no faults.


### -field VolumeStateNoDirectIO

Direct I/O is disabled for the CSV.


### -field VolumeStateNoAccess

The CSV can not be accessed.


### -field VolumeStateInMaintenance

The CSV is in maintenance mode.


### -field VolumeStateDismounted

The CSV is dismounted.


## -see-also




<a href="https://msdn.microsoft.com/C672B42B-0DB9-4E70-8157-15C3189102EF">CLUS_CSV_VOLUME_INFO</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

