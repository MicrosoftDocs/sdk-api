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

# _SR_RESOURCE_TYPE_ELIGIBLE_TARGET_DATADISKS structure


## -description


Describes a set of retrieved data disks that can be used as target sites for replication.


## -struct-fields




### -field SourceDataDiskGuid

The cluster resource identifier of the data disk.


### -field TargetReplicationGroupGuid

The identifier of the replication group that contains the retrieved data disks.


### -field SkipConnectivityCheck

<b>true</b> if the disks that are connected to the same nodes as the source disk are included in result set.


### -field IncludeOfflineDisks

<b>true</b> if the result set includes all offline disks in the available storage group.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

