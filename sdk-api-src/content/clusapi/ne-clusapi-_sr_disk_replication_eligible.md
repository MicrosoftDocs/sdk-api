---
UID: NE:clusapi._SR_DISK_REPLICATION_ELIGIBLE
title: "_SR_DISK_REPLICATION_ELIGIBLE"
author: windows-sdk-content
description: Specifies the various reasons a disk on a cluster node can be eligible or ineligible for replication.
old-location: mscs\sr_disk_replication_eligible.htm
tech.root: mscs
ms.assetid: 3B38E2C8-CF41-4630-8AA8-72581D1DC264
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*PSR_DISK_REPLICATION_ELIGIBLE, SR_DISK_REPLICATION_ELIGIBLE, SR_DISK_REPLICATION_ELIGIBLE enumeration [Failover Cluster], SrDiskReplicationEligibleAlreadyInReplication, SrDiskReplicationEligibleFileSystemNotSupported, SrDiskReplicationEligibleInSameSite, SrDiskReplicationEligibleInsufficientFreeSpace, SrDiskReplicationEligibleNone, SrDiskReplicationEligibleNotGpt, SrDiskReplicationEligibleNotInSameSite, SrDiskReplicationEligibleOffline, SrDiskReplicationEligibleOther, SrDiskReplicationEligiblePartitionLayoutMismatch, SrDiskReplicationEligibleSameAsSpecifiedDisk, SrDiskReplicationEligibleYes, _SR_DISK_REPLICATION_ELIGIBLE, clusapi/SR_DISK_REPLICATION_ELIGIBLE, clusapi/SrDiskReplicationEligibleAlreadyInReplication, clusapi/SrDiskReplicationEligibleFileSystemNotSupported, clusapi/SrDiskReplicationEligibleInSameSite, clusapi/SrDiskReplicationEligibleInsufficientFreeSpace, clusapi/SrDiskReplicationEligibleNone, clusapi/SrDiskReplicationEligibleNotGpt, clusapi/SrDiskReplicationEligibleNotInSameSite, clusapi/SrDiskReplicationEligibleOffline, clusapi/SrDiskReplicationEligibleOther, clusapi/SrDiskReplicationEligiblePartitionLayoutMismatch, clusapi/SrDiskReplicationEligibleSameAsSpecifiedDisk, clusapi/SrDiskReplicationEligibleYes, msclus/SR_DISK_REPLICATION_ELIGIBLE, msclus/SrDiskReplicationEligibleAlreadyInReplication, msclus/SrDiskReplicationEligibleFileSystemNotSupported, msclus/SrDiskReplicationEligibleInSameSite, msclus/SrDiskReplicationEligibleInsufficientFreeSpace, msclus/SrDiskReplicationEligibleNone, msclus/SrDiskReplicationEligibleNotGpt, msclus/SrDiskReplicationEligibleNotInSameSite, msclus/SrDiskReplicationEligibleOffline, msclus/SrDiskReplicationEligibleOther, msclus/SrDiskReplicationEligiblePartitionLayoutMismatch, msclus/SrDiskReplicationEligibleSameAsSpecifiedDisk, msclus/SrDiskReplicationEligibleYes, mscs.sr_disk_replication_eligible"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - MsClus.h
api_name:
 - SR_DISK_REPLICATION_ELIGIBLE
product: Windows
targetos: Windows
req.typenames: SR_DISK_REPLICATION_ELIGIBLE, *PSR_DISK_REPLICATION_ELIGIBLE
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt421319(v=VS.85).aspx">SR_RESOURCE_TYPE_DISK_INFO</a>
 

 

