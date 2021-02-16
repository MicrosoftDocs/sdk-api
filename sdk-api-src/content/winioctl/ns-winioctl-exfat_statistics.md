---
UID: NS:winioctl._EXFAT_STATISTICS
title: EXFAT_STATISTICS
description: Contains statistical information from the exFAT file system.
helpviewer_keywords: ["*PEXFAT_STATISTICS","EXFAT_STATISTICS","EXFAT_STATISTICS structure [Files]","PEXFAT_STATISTICS","PEXFAT_STATISTICS structure pointer [Files]","fs.exfat_statistics","winioctl/EXFAT_STATISTICS","winioctl/PEXFAT_STATISTICS"]
old-location: fs\exfat_statistics.htm
tech.root: fs
ms.assetid: fc33e967-fbc0-4f98-9b6c-2d6ac103a256
ms.date: 12/05/2018
ms.keywords: '*PEXFAT_STATISTICS, EXFAT_STATISTICS, EXFAT_STATISTICS structure [Files], PEXFAT_STATISTICS, PEXFAT_STATISTICS structure pointer [Files], fs.exfat_statistics, winioctl/EXFAT_STATISTICS, winioctl/PEXFAT_STATISTICS'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EXFAT_STATISTICS, *PEXFAT_STATISTICS
req.redist: 
f1_keywords:
 - _EXFAT_STATISTICS
 - winioctl/_EXFAT_STATISTICS
 - PEXFAT_STATISTICS
 - winioctl/PEXFAT_STATISTICS
 - EXFAT_STATISTICS
 - winioctl/EXFAT_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - EXFAT_STATISTICS
---

# EXFAT_STATISTICS structure


## -description

Contains statistical information from the exFAT file system.

## -struct-fields

### -field CreateHits

The number of create operations.

### -field SuccessfulCreates

The number of successful create operations.

### -field FailedCreates

The number of failed create operations.

### -field NonCachedReads

The number of read operations that were not cached.

### -field NonCachedReadBytes

The number of bytes read from a file that were not cached.

### -field NonCachedWrites

The number of write operations that were not cached.

### -field NonCachedWriteBytes

The number of bytes written to a file that were not cached.

### -field NonCachedDiskReads

The number of read operations that were not cached. This value includes sub-read operations.

### -field NonCachedDiskWrites

The number of write operations that were not cached. This value includes sub-write operations.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-fat_statistics">FAT_STATISTICS</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-filesystem_statistics">FILESYSTEM_STATISTICS</a>