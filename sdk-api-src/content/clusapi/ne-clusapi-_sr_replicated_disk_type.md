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

# _SR_REPLICATED_DISK_TYPE enumeration


## -description


Specifies the replicated disk types for the <a href="https://msdn.microsoft.com/0C020CC3-43CD-49ED-B42D-2365D76ED40D">SR_RESOURCE_TYPE_REPLICATED_DISK</a> structure.


## -enum-fields




### -field SrReplicatedDiskTypeNone

None.


### -field SrReplicatedDiskTypeSource

The source of replication.


### -field SrReplicatedDiskTypeLogSource

A log disk that is the source of replication.


### -field SrReplicatedDiskTypeDestination

The destination of replication.


### -field SrReplicatedDiskTypeLogDestination

A log disk that is the destination of replication.


### -field SrReplicatedDiskTypeNotInParthership

The disk is not in a replication partnership.


### -field SrReplicatedDiskTypeLogNotInParthership

A log disk that is not in a replication partnership.


### -field SrReplicatedDiskTypeOther

Other.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

