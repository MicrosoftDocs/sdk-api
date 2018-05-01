---
UID: NS:clusapi._CLUS_STORAGE_REMAP_DRIVELETTER
title: "_CLUS_STORAGE_REMAP_DRIVELETTER"
author: windows-driver-content
description: Identifies the existing and target drive letter for a disk drive on a node.
old-location: mscs\clus_storage_remap_driveletter.htm
old-project: MsCS
ms.assetid: b79e4aa0-fca3-4b9c-9e3f-73cd627752a2
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PCLUS_STORAGE_REMAP_DRIVELETTER, CLUS_STORAGE_REMAP_DRIVELETTER, CLUS_STORAGE_REMAP_DRIVELETTER structure [Failover Cluster], PCLUS_STORAGE_REMAP_DRIVELETTER, PCLUS_STORAGE_REMAP_DRIVELETTER structure pointer [Failover Cluster], _CLUS_STORAGE_REMAP_DRIVELETTER, clusapi/CLUS_STORAGE_REMAP_DRIVELETTER, clusapi/PCLUS_STORAGE_REMAP_DRIVELETTER, mscs.clus_storage_remap_driveletter"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CLUS_STORAGE_REMAP_DRIVELETTER, *PCLUS_STORAGE_REMAP_DRIVELETTER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusAPI.h
api_name:
-	CLUS_STORAGE_REMAP_DRIVELETTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CLUS_STORAGE_REMAP_DRIVELETTER structure


## -description


Identifies the existing and target drive letter for a disk drive on a node.


## -struct-fields




### -field CurrentDriveLetterMask

A 32-bit bitmask indicating the drive letter to be changed. The least significant bit represents the drive letter 'A' through bit 25, which represents the drive letter 'Z'.


### -field TargetDriveLetterMask

A 32-bit bitmask indicating the new drive letter for the disk drive that corresponds to the drive letter specified in CurrentDriveLetterMask.

