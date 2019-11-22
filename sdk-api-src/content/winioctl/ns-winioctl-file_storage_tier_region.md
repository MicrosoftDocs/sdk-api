---
UID: NS:winioctl._FILE_STORAGE_TIER_REGION
title: FILE_STORAGE_TIER_REGION

description: Describes a single storage tier region.
old-location: fs\file_storage_tier_region.htm
tech.root: FileIO
ms.assetid: 5178A987-397A-44E5-9485-221D72490124

ms.date: 12/05/2018
ms.keywords: "*PFILE_STORAGE_TIER_REGION, FILE_STORAGE_TIER_REGION, FILE_STORAGE_TIER_REGION structure [Files], PFILE_STORAGE_TIER_REGION, PFILE_STORAGE_TIER_REGION structure pointer [Files], fs.file_storage_tier_region, winioctl/FILE_STORAGE_TIER_REGION, winioctl/PFILE_STORAGE_TIER_REGION"
ms.topic: struct
f1_keywords: 
 - "winioctl/FILE_STORAGE_TIER_REGION"
dev_langs:
 - c++
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
 - WinIoctl.h
api_name:
 - FILE_STORAGE_TIER_REGION
targetos: Windows
req.typenames: FILE_STORAGE_TIER_REGION, *PFILE_STORAGE_TIER_REGION
req.redist: 
---

# FILE_STORAGE_TIER_REGION structure


## -description


Describes a single storage tier region.


## -struct-fields




### -field TierId

Tier ID.


### -field Offset

Offset from the beginning of the volume of this region, in bytes.


### -field Length

Length of region in bytes.

