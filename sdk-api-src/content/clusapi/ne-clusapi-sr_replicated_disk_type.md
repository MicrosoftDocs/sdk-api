---
UID: NE:clusapi._SR_REPLICATED_DISK_TYPE
title: SR_REPLICATED_DISK_TYPE (clusapi.h)
description: Specifies the replicated disk types for the SR_RESOURCE_TYPE_REPLICATED_DISK structure.
helpviewer_keywords: ["*PSR_REPLICATED_DISK_TYPE","PSR_REPLICATED_DISK_TYPE","PSR_REPLICATED_DISK_TYPE enumeration pointer [Failover Cluster]","SR_REPLICATED_DISK_TYPE","SR_REPLICATED_DISK_TYPE enumeration [Failover Cluster]","SrReplicatedDiskTypeDestination","SrReplicatedDiskTypeLogDestination","SrReplicatedDiskTypeLogNotInParthership","SrReplicatedDiskTypeLogSource","SrReplicatedDiskTypeNone","SrReplicatedDiskTypeNotInParthership","SrReplicatedDiskTypeOther","SrReplicatedDiskTypeSource","clusapi/PSR_REPLICATED_DISK_TYPE","clusapi/SR_REPLICATED_DISK_TYPE","clusapi/SrReplicatedDiskTypeDestination","clusapi/SrReplicatedDiskTypeLogDestination","clusapi/SrReplicatedDiskTypeLogNotInParthership","clusapi/SrReplicatedDiskTypeLogSource","clusapi/SrReplicatedDiskTypeNone","clusapi/SrReplicatedDiskTypeNotInParthership","clusapi/SrReplicatedDiskTypeOther","clusapi/SrReplicatedDiskTypeSource","mscs.sr_replicated_disk_type","resapi/PSR_REPLICATED_DISK_TYPE","resapi/SR_REPLICATED_DISK_TYPE","resapi/SrReplicatedDiskTypeDestination","resapi/SrReplicatedDiskTypeLogDestination","resapi/SrReplicatedDiskTypeLogNotInParthership","resapi/SrReplicatedDiskTypeLogSource","resapi/SrReplicatedDiskTypeNone","resapi/SrReplicatedDiskTypeNotInParthership","resapi/SrReplicatedDiskTypeOther","resapi/SrReplicatedDiskTypeSource"]
old-location: mscs\sr_replicated_disk_type.htm
tech.root: MsCS
ms.assetid: 913367E0-B3C2-40D0-B516-6C2F834152BB
ms.date: 12/05/2018
ms.keywords: '*PSR_REPLICATED_DISK_TYPE, PSR_REPLICATED_DISK_TYPE, PSR_REPLICATED_DISK_TYPE enumeration pointer [Failover Cluster], SR_REPLICATED_DISK_TYPE, SR_REPLICATED_DISK_TYPE enumeration [Failover Cluster], SrReplicatedDiskTypeDestination, SrReplicatedDiskTypeLogDestination, SrReplicatedDiskTypeLogNotInParthership, SrReplicatedDiskTypeLogSource, SrReplicatedDiskTypeNone, SrReplicatedDiskTypeNotInParthership, SrReplicatedDiskTypeOther, SrReplicatedDiskTypeSource, clusapi/PSR_REPLICATED_DISK_TYPE, clusapi/SR_REPLICATED_DISK_TYPE, clusapi/SrReplicatedDiskTypeDestination, clusapi/SrReplicatedDiskTypeLogDestination, clusapi/SrReplicatedDiskTypeLogNotInParthership, clusapi/SrReplicatedDiskTypeLogSource, clusapi/SrReplicatedDiskTypeNone, clusapi/SrReplicatedDiskTypeNotInParthership, clusapi/SrReplicatedDiskTypeOther, clusapi/SrReplicatedDiskTypeSource, mscs.sr_replicated_disk_type, resapi/PSR_REPLICATED_DISK_TYPE, resapi/SR_REPLICATED_DISK_TYPE, resapi/SrReplicatedDiskTypeDestination, resapi/SrReplicatedDiskTypeLogDestination, resapi/SrReplicatedDiskTypeLogNotInParthership, resapi/SrReplicatedDiskTypeLogSource, resapi/SrReplicatedDiskTypeNone, resapi/SrReplicatedDiskTypeNotInParthership, resapi/SrReplicatedDiskTypeOther, resapi/SrReplicatedDiskTypeSource'
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SR_REPLICATED_DISK_TYPE
 - clusapi/_SR_REPLICATED_DISK_TYPE
 - PSR_REPLICATED_DISK_TYPE
 - clusapi/PSR_REPLICATED_DISK_TYPE
 - SR_REPLICATED_DISK_TYPE
 - clusapi/SR_REPLICATED_DISK_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
 - ClusApi.h
api_name:
 - SR_REPLICATED_DISK_TYPE
---

# SR_REPLICATED_DISK_TYPE enumeration


## -description

Specifies the replicated disk types for the <a href="/windows/desktop/api/clusapi/ns-clusapi-sr_resource_type_replicated_disk">SR_RESOURCE_TYPE_REPLICATED_DISK</a> structure.

## -enum-fields

### -field SrReplicatedDiskTypeNone:0

None.

### -field SrReplicatedDiskTypeSource:1

The source of replication.

### -field SrReplicatedDiskTypeLogSource:2

A log disk that is the source of replication.

### -field SrReplicatedDiskTypeDestination:3

The destination of replication.

### -field SrReplicatedDiskTypeLogDestination:4

A log disk that is the destination of replication.

### -field SrReplicatedDiskTypeNotInParthership:5

The disk is not in a replication partnership.

### -field SrReplicatedDiskTypeLogNotInParthership:6

A log disk that is not in a replication partnership.

### -field SrReplicatedDiskTypeOther

Other.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
