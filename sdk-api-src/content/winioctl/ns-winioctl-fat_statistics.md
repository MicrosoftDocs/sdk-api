---
UID: NS:winioctl._FAT_STATISTICS
title: FAT_STATISTICS
author: windows-sdk-content
description: Contains statistical information from the FAT file system.
old-location: fs\fat_statistics_str.htm
tech.root: FileIO
ms.assetid: 98d293e8-e708-48f5-99b1-603f27e6ef16
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFAT_STATISTICS, FAT_STATISTICS, FAT_STATISTICS structure [Files], PFAT_STATISTICS, PFAT_STATISTICS structure pointer [Files], base.fat_statistics_str, fs.fat_statistics_str, winioctl/FAT_STATISTICS, winioctl/PFAT_STATISTICS"
ms.topic: struct
f1_keywords: 
 - "winioctl/FAT_STATISTICS"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FAT_STATISTICS
product: Windows
targetos: Windows
req.typenames: FAT_STATISTICS, *PFAT_STATISTICS
req.redist: 
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




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_exfat_statistics">EXFAT_STATISTICS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_filesystem_statistics">FILESYSTEM_STATISTICS</a>
 

 

