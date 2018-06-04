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

# _SR_DISK_REPLICATION_ELIGIBLE enumeration


## -description


Specifies the various reasons a disk on a cluster node can be eligible or ineligible for replication.


## -enum-fields




### -field SrDiskReplicationEligibleNone

None of the disks on the node are eligible for replication.


### -field SrDiskReplicationEligibleYes

The disk is eligible for replication.


### -field SrDiskReplicationEligibleOffline

The disk is offline.


### -field SrDiskReplicationEligibleNotGpt

The disk is not formatted with a GUID partition table (GPT).


### -field SrDiskReplicationEligiblePartitionLayoutMismatch

There are a different number of target and source partitions.


### -field SrDiskReplicationEligibleInsufficientFreeSpace

There is not enough free space on the disk.


### -field SrDiskReplicationEligibleNotInSameSite

The disk is not on the same site at the target disk.


### -field SrDiskReplicationEligibleInSameSite

The disk is on the same site as the target disk.


### -field SrDiskReplicationEligibleFileSystemNotSupported

The file system on the disk is not supported.


### -field SrDiskReplicationEligibleAlreadyInReplication

The disk is already being replicated.


### -field SrDiskReplicationEligibleSameAsSpecifiedDisk

The disk is the target disk.


### -field SrDiskReplicationEligibleOther

Other.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/8A53714D-D125-4B83-B51D-DF0EADE4C4E0">SR_RESOURCE_TYPE_DISK_INFO</a>
 

 

