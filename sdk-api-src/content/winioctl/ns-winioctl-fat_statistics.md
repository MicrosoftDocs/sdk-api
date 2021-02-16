---
UID: NS:winioctl._FAT_STATISTICS
title: FAT_STATISTICS
description: Contains statistical information from the FAT file system.
helpviewer_keywords: ["*PFAT_STATISTICS","FAT_STATISTICS","FAT_STATISTICS structure [Files]","PFAT_STATISTICS","PFAT_STATISTICS structure pointer [Files]","base.fat_statistics_str","fs.fat_statistics_str","winioctl/FAT_STATISTICS","winioctl/PFAT_STATISTICS"]
old-location: fs\fat_statistics_str.htm
tech.root: fs
ms.assetid: 98d293e8-e708-48f5-99b1-603f27e6ef16
ms.date: 12/05/2018
ms.keywords: '*PFAT_STATISTICS, FAT_STATISTICS, FAT_STATISTICS structure [Files], PFAT_STATISTICS, PFAT_STATISTICS structure pointer [Files], base.fat_statistics_str, fs.fat_statistics_str, winioctl/FAT_STATISTICS, winioctl/PFAT_STATISTICS'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: FAT_STATISTICS, *PFAT_STATISTICS
req.redist: 
f1_keywords:
 - _FAT_STATISTICS
 - winioctl/_FAT_STATISTICS
 - PFAT_STATISTICS
 - winioctl/PFAT_STATISTICS
 - FAT_STATISTICS
 - winioctl/FAT_STATISTICS
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
 - FAT_STATISTICS
---

# FAT_STATISTICS structure


## -description

Contains statistical information from the FAT file system.

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

<a href="/windows/desktop/api/winioctl/ns-winioctl-exfat_statistics">EXFAT_STATISTICS</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-filesystem_statistics">FILESYSTEM_STATISTICS</a>