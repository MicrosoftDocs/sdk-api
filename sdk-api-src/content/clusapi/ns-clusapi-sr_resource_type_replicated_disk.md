---
UID: NS:clusapi._SR_RESOURCE_TYPE_REPLICATED_DISK
title: SR_RESOURCE_TYPE_REPLICATED_DISK (clusapi.h)
description: Represents a replicated disk.
helpviewer_keywords: ["*PSR_RESOURCE_TYPE_REPLICATED_DISK","PSR_RESOURCE_TYPE_REPLICATED_DISK","PSR_RESOURCE_TYPE_REPLICATED_DISK structure pointer [Failover Cluster]","SR_RESOURCE_TYPE_REPLICATED_DISK","SR_RESOURCE_TYPE_REPLICATED_DISK structure [Failover Cluster]","clusapi/PSR_RESOURCE_TYPE_REPLICATED_DISK","clusapi/SR_RESOURCE_TYPE_REPLICATED_DISK","mscs.sr_resource_type_replicated_disk"]
old-location: mscs\sr_resource_type_replicated_disk.htm
tech.root: MsCS
ms.assetid: 0C020CC3-43CD-49ED-B42D-2365D76ED40D
ms.date: 12/05/2018
ms.keywords: '*PSR_RESOURCE_TYPE_REPLICATED_DISK, PSR_RESOURCE_TYPE_REPLICATED_DISK, PSR_RESOURCE_TYPE_REPLICATED_DISK structure pointer [Failover Cluster], SR_RESOURCE_TYPE_REPLICATED_DISK, SR_RESOURCE_TYPE_REPLICATED_DISK structure [Failover Cluster], clusapi/PSR_RESOURCE_TYPE_REPLICATED_DISK, clusapi/SR_RESOURCE_TYPE_REPLICATED_DISK, mscs.sr_resource_type_replicated_disk'
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
req.typenames: SR_RESOURCE_TYPE_REPLICATED_DISK, *PSR_RESOURCE_TYPE_REPLICATED_DISK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SR_RESOURCE_TYPE_REPLICATED_DISK
 - clusapi/_SR_RESOURCE_TYPE_REPLICATED_DISK
 - PSR_RESOURCE_TYPE_REPLICATED_DISK
 - clusapi/PSR_RESOURCE_TYPE_REPLICATED_DISK
 - SR_RESOURCE_TYPE_REPLICATED_DISK
 - clusapi/SR_RESOURCE_TYPE_REPLICATED_DISK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - SR_RESOURCE_TYPE_REPLICATED_DISK
---

# SR_RESOURCE_TYPE_REPLICATED_DISK structure


## -description

Represents a replicated disk.

## -struct-fields

### -field Type

The type of the replicated disk.

### -field ClusterDiskResourceGuid

The cluster resource identifier of the disk.

### -field ReplicationGroupId

The replication group identifier of the disk.

### -field ReplicationGroupName

The name of the replication group..

## -see-also

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>



<a href="/windows/desktop/api/clusapi/ne-clusapi-sr_replicated_disk_type">SR_REPLICATED_DISK_TYPE</a>