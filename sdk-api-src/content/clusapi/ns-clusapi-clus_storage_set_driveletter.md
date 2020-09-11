---
UID: NS:clusapi._CLUS_STORAGE_SET_DRIVELETTER
title: CLUS_STORAGE_SET_DRIVELETTER (clusapi.h)
description: Supplies drive letter information for a disk partition associated with a storage class resource.
helpviewer_keywords: ["*PCLUS_STORAGE_SET_DRIVELETTER","CLUS_STORAGE_SET_DRIVELETTER","CLUS_STORAGE_SET_DRIVELETTER structure [Failover Cluster]","PCLUS_STORAGE_SET_DRIVELETTER","PCLUS_STORAGE_SET_DRIVELETTER structure pointer [Failover Cluster]","clusapi/CLUS_STORAGE_SET_DRIVELETTER","clusapi/PCLUS_STORAGE_SET_DRIVELETTER","mscs.clus_storage_set_driveletter"]
old-location: mscs\clus_storage_set_driveletter.htm
tech.root: MsCS
ms.assetid: 71f3a009-c4af-4c7a-973d-4bd2eba25b94
ms.date: 12/05/2018
ms.keywords: '*PCLUS_STORAGE_SET_DRIVELETTER, CLUS_STORAGE_SET_DRIVELETTER, CLUS_STORAGE_SET_DRIVELETTER structure [Failover Cluster], PCLUS_STORAGE_SET_DRIVELETTER, PCLUS_STORAGE_SET_DRIVELETTER structure pointer [Failover Cluster], clusapi/CLUS_STORAGE_SET_DRIVELETTER, clusapi/PCLUS_STORAGE_SET_DRIVELETTER, mscs.clus_storage_set_driveletter'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
req.typenames: CLUS_STORAGE_SET_DRIVELETTER, *PCLUS_STORAGE_SET_DRIVELETTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUS_STORAGE_SET_DRIVELETTER
 - clusapi/_CLUS_STORAGE_SET_DRIVELETTER
 - PCLUS_STORAGE_SET_DRIVELETTER
 - clusapi/PCLUS_STORAGE_SET_DRIVELETTER
 - CLUS_STORAGE_SET_DRIVELETTER
 - clusapi/CLUS_STORAGE_SET_DRIVELETTER
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
 - CLUS_STORAGE_SET_DRIVELETTER
---

# CLUS_STORAGE_SET_DRIVELETTER structure


## -description

Supplies drive letter information for a disk partition associated with a storage class resource.

## -struct-fields

### -field PartitionNumber

A 32-bit integer that indicates a partition on the storage device.

### -field DriveLetterMask

A 32-bit integer bitmask that indicates either the new drive letter of the partition or that the partition's drive letter should be removed. Each bit represents a drive letter where bit 0 represents 'A', bit 1 represents 'B', and so forth through bit 25. Bits 26 through 31 are ignored. A value of zero indicates that the drive letter should be removed.

