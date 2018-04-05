---
UID: NS:winioctl._FILE_STORAGE_TIER_REGION
title: "_FILE_STORAGE_TIER_REGION"
author: windows-driver-content
description: Describes a single storage tier region.
old-location: fs\file_storage_tier_region.htm
old-project: FileIO
ms.assetid: 5178A987-397A-44E5-9485-221D72490124
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PFILE_STORAGE_TIER_REGION, FILE_STORAGE_TIER_REGION, FILE_STORAGE_TIER_REGION structure [Files], PFILE_STORAGE_TIER_REGION, PFILE_STORAGE_TIER_REGION structure pointer [Files], _FILE_STORAGE_TIER_REGION, fs.file_storage_tier_region, winioctl/FILE_STORAGE_TIER_REGION, winioctl/PFILE_STORAGE_TIER_REGION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: FILE_STORAGE_TIER_REGION, *PFILE_STORAGE_TIER_REGION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoctl.h
api_name:
-	FILE_STORAGE_TIER_REGION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_STORAGE_TIER_REGION structure


## -description


Describes a single storage tier region.


## -struct-fields




### -field TierId

Tier ID.


### -field Offset

Offset from the beginning of the volume of this region, in bytes.


### -field Length

Length of region in bytes.

