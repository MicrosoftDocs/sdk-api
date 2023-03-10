---
UID: NS:clusapi._CLUS_STORAGE_REMAP_DRIVELETTER
title: CLUS_STORAGE_REMAP_DRIVELETTER (clusapi.h)
description: Identifies the existing and target drive letter for a disk drive on a node.
helpviewer_keywords: ["*PCLUS_STORAGE_REMAP_DRIVELETTER","CLUS_STORAGE_REMAP_DRIVELETTER","CLUS_STORAGE_REMAP_DRIVELETTER structure [Failover Cluster]","PCLUS_STORAGE_REMAP_DRIVELETTER","PCLUS_STORAGE_REMAP_DRIVELETTER structure pointer [Failover Cluster]","clusapi/CLUS_STORAGE_REMAP_DRIVELETTER","clusapi/PCLUS_STORAGE_REMAP_DRIVELETTER","mscs.clus_storage_remap_driveletter"]
old-location: mscs\clus_storage_remap_driveletter.htm
tech.root: MsCS
ms.assetid: b79e4aa0-fca3-4b9c-9e3f-73cd627752a2
ms.date: 12/05/2018
ms.keywords: '*PCLUS_STORAGE_REMAP_DRIVELETTER, CLUS_STORAGE_REMAP_DRIVELETTER, CLUS_STORAGE_REMAP_DRIVELETTER structure [Failover Cluster], PCLUS_STORAGE_REMAP_DRIVELETTER, PCLUS_STORAGE_REMAP_DRIVELETTER structure pointer [Failover Cluster], clusapi/CLUS_STORAGE_REMAP_DRIVELETTER, clusapi/PCLUS_STORAGE_REMAP_DRIVELETTER, mscs.clus_storage_remap_driveletter'
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
req.typenames: CLUS_STORAGE_REMAP_DRIVELETTER, *PCLUS_STORAGE_REMAP_DRIVELETTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUS_STORAGE_REMAP_DRIVELETTER
 - clusapi/_CLUS_STORAGE_REMAP_DRIVELETTER
 - PCLUS_STORAGE_REMAP_DRIVELETTER
 - clusapi/PCLUS_STORAGE_REMAP_DRIVELETTER
 - CLUS_STORAGE_REMAP_DRIVELETTER
 - clusapi/CLUS_STORAGE_REMAP_DRIVELETTER
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
 - CLUS_STORAGE_REMAP_DRIVELETTER
---

# CLUS_STORAGE_REMAP_DRIVELETTER structure


## -description

Identifies the existing and target drive letter for a disk drive on a node.

## -struct-fields

### -field CurrentDriveLetterMask

A 32-bit bitmask indicating the drive letter to be changed. The least significant bit represents the drive letter 'A' through bit 25, which represents the drive letter 'Z'.

### -field TargetDriveLetterMask

A 32-bit bitmask indicating the new drive letter for the disk drive that corresponds to the drive letter specified in CurrentDriveLetterMask.

