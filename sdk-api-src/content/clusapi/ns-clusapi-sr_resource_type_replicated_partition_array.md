---
UID: NS:clusapi._SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY
title: SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY (clusapi.h)
description: Lists the all replicated partitions on a disk.
helpviewer_keywords: ["*PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY","PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY","PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY structure pointer [Failover Cluster]","SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY","SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY structure [Failover Cluster]","clusapi/PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY","clusapi/SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY","mscs.sr_resource_type_replicated_partition_array"]
old-location: mscs\sr_resource_type_replicated_partition_array.htm
tech.root: MsCS
ms.assetid: 3FD68FF6-3377-4EBF-95F4-94835ABB1274
ms.date: 12/05/2018
ms.keywords: '*PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY, PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY, PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY structure pointer [Failover Cluster], SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY, SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY structure [Failover Cluster], clusapi/PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY, clusapi/SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY, mscs.sr_resource_type_replicated_partition_array'
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
req.typenames: SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY, *PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY
 - clusapi/_SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY
 - PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY
 - clusapi/PSR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY
 - SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY
 - clusapi/SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY
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
 - SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY
---

# SR_RESOURCE_TYPE_REPLICATED_PARTITION_ARRAY structure


## -description

Lists the all replicated partitions on a disk.

## -struct-fields

### -field Count

The count of all replicated partitions on the disk.

### -field PartitionArray

A variable size array of all replicated partitions on the disk.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>