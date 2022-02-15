---
UID: NE:clusapi._SR_DISK_REPLICATION_ELIGIBLE
title: SR_DISK_REPLICATION_ELIGIBLE (clusapi.h)
description: Specifies the various reasons a disk on a cluster node can be eligible or ineligible for replication.
helpviewer_keywords: ["*PSR_DISK_REPLICATION_ELIGIBLE","SR_DISK_REPLICATION_ELIGIBLE","SR_DISK_REPLICATION_ELIGIBLE enumeration [Failover Cluster]","SrDiskReplicationEligibleAlreadyInReplication","SrDiskReplicationEligibleFileSystemNotSupported","SrDiskReplicationEligibleInSameSite","SrDiskReplicationEligibleInsufficientFreeSpace","SrDiskReplicationEligibleNone","SrDiskReplicationEligibleNotGpt","SrDiskReplicationEligibleNotInSameSite","SrDiskReplicationEligibleOffline","SrDiskReplicationEligibleOther","SrDiskReplicationEligiblePartitionLayoutMismatch","SrDiskReplicationEligibleSameAsSpecifiedDisk","SrDiskReplicationEligibleYes","clusapi/SR_DISK_REPLICATION_ELIGIBLE","clusapi/SrDiskReplicationEligibleAlreadyInReplication","clusapi/SrDiskReplicationEligibleFileSystemNotSupported","clusapi/SrDiskReplicationEligibleInSameSite","clusapi/SrDiskReplicationEligibleInsufficientFreeSpace","clusapi/SrDiskReplicationEligibleNone","clusapi/SrDiskReplicationEligibleNotGpt","clusapi/SrDiskReplicationEligibleNotInSameSite","clusapi/SrDiskReplicationEligibleOffline","clusapi/SrDiskReplicationEligibleOther","clusapi/SrDiskReplicationEligiblePartitionLayoutMismatch","clusapi/SrDiskReplicationEligibleSameAsSpecifiedDisk","clusapi/SrDiskReplicationEligibleYes","msclus/SR_DISK_REPLICATION_ELIGIBLE","msclus/SrDiskReplicationEligibleAlreadyInReplication","msclus/SrDiskReplicationEligibleFileSystemNotSupported","msclus/SrDiskReplicationEligibleInSameSite","msclus/SrDiskReplicationEligibleInsufficientFreeSpace","msclus/SrDiskReplicationEligibleNone","msclus/SrDiskReplicationEligibleNotGpt","msclus/SrDiskReplicationEligibleNotInSameSite","msclus/SrDiskReplicationEligibleOffline","msclus/SrDiskReplicationEligibleOther","msclus/SrDiskReplicationEligiblePartitionLayoutMismatch","msclus/SrDiskReplicationEligibleSameAsSpecifiedDisk","msclus/SrDiskReplicationEligibleYes","mscs.sr_disk_replication_eligible"]
old-location: mscs\sr_disk_replication_eligible.htm
tech.root: MsCS
ms.assetid: 3B38E2C8-CF41-4630-8AA8-72581D1DC264
ms.date: 12/05/2018
ms.keywords: '*PSR_DISK_REPLICATION_ELIGIBLE, SR_DISK_REPLICATION_ELIGIBLE, SR_DISK_REPLICATION_ELIGIBLE enumeration [Failover Cluster], SrDiskReplicationEligibleAlreadyInReplication, SrDiskReplicationEligibleFileSystemNotSupported, SrDiskReplicationEligibleInSameSite, SrDiskReplicationEligibleInsufficientFreeSpace, SrDiskReplicationEligibleNone, SrDiskReplicationEligibleNotGpt, SrDiskReplicationEligibleNotInSameSite, SrDiskReplicationEligibleOffline, SrDiskReplicationEligibleOther, SrDiskReplicationEligiblePartitionLayoutMismatch, SrDiskReplicationEligibleSameAsSpecifiedDisk, SrDiskReplicationEligibleYes, clusapi/SR_DISK_REPLICATION_ELIGIBLE, clusapi/SrDiskReplicationEligibleAlreadyInReplication, clusapi/SrDiskReplicationEligibleFileSystemNotSupported, clusapi/SrDiskReplicationEligibleInSameSite, clusapi/SrDiskReplicationEligibleInsufficientFreeSpace, clusapi/SrDiskReplicationEligibleNone, clusapi/SrDiskReplicationEligibleNotGpt, clusapi/SrDiskReplicationEligibleNotInSameSite, clusapi/SrDiskReplicationEligibleOffline, clusapi/SrDiskReplicationEligibleOther, clusapi/SrDiskReplicationEligiblePartitionLayoutMismatch, clusapi/SrDiskReplicationEligibleSameAsSpecifiedDisk, clusapi/SrDiskReplicationEligibleYes, msclus/SR_DISK_REPLICATION_ELIGIBLE, msclus/SrDiskReplicationEligibleAlreadyInReplication, msclus/SrDiskReplicationEligibleFileSystemNotSupported, msclus/SrDiskReplicationEligibleInSameSite, msclus/SrDiskReplicationEligibleInsufficientFreeSpace, msclus/SrDiskReplicationEligibleNone, msclus/SrDiskReplicationEligibleNotGpt, msclus/SrDiskReplicationEligibleNotInSameSite, msclus/SrDiskReplicationEligibleOffline, msclus/SrDiskReplicationEligibleOther, msclus/SrDiskReplicationEligiblePartitionLayoutMismatch, msclus/SrDiskReplicationEligibleSameAsSpecifiedDisk, msclus/SrDiskReplicationEligibleYes, mscs.sr_disk_replication_eligible'
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
targetos: Windows
req.typenames: SR_DISK_REPLICATION_ELIGIBLE, *PSR_DISK_REPLICATION_ELIGIBLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SR_DISK_REPLICATION_ELIGIBLE
 - clusapi/_SR_DISK_REPLICATION_ELIGIBLE
 - PSR_DISK_REPLICATION_ELIGIBLE
 - clusapi/PSR_DISK_REPLICATION_ELIGIBLE
 - SR_DISK_REPLICATION_ELIGIBLE
 - clusapi/SR_DISK_REPLICATION_ELIGIBLE
dev_langs:
 - c++
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
---

# SR_DISK_REPLICATION_ELIGIBLE enumeration


## -description

Specifies the various reasons a disk on a cluster node can be eligible or ineligible for replication.

## -enum-fields

### -field SrDiskReplicationEligibleNone:0

None of the disks on the node are eligible for replication.

### -field SrDiskReplicationEligibleYes:1

The disk is eligible for replication.

### -field SrDiskReplicationEligibleOffline:2

The disk is offline.

### -field SrDiskReplicationEligibleNotGpt:3

The disk is not formatted with a GUID partition table (GPT).

### -field SrDiskReplicationEligiblePartitionLayoutMismatch:4

There are a different number of target and source partitions.

### -field SrDiskReplicationEligibleInsufficientFreeSpace:5

There is not enough free space on the disk.

### -field SrDiskReplicationEligibleNotInSameSite:6

The disk is not on the same site at the target disk.

### -field SrDiskReplicationEligibleInSameSite:7

The disk is on the same site as the target disk.

### -field SrDiskReplicationEligibleFileSystemNotSupported:8

The file system on the disk is not supported.

### -field SrDiskReplicationEligibleAlreadyInReplication:9

The disk is already being replicated.

### -field SrDiskReplicationEligibleSameAsSpecifiedDisk:10

The disk is the target disk.

### -field SrDiskReplicationEligibleOther:9999

Other.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/windows/desktop/api/clusapi/ns-clusapi-sr_resource_type_disk_info">SR_RESOURCE_TYPE_DISK_INFO</a>
