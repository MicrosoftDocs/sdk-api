---
UID: NS:winioctl._EXFAT_STATISTICS
title: "_EXFAT_STATISTICS"
author: windows-sdk-content
description: Contains statistical information from the exFAT file system.
old-location: fs\exfat_statistics.htm
tech.root: fileio
ms.assetid: fc33e967-fbc0-4f98-9b6c-2d6ac103a256
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PEXFAT_STATISTICS, EXFAT_STATISTICS, EXFAT_STATISTICS structure [Files], PEXFAT_STATISTICS, PEXFAT_STATISTICS structure pointer [Files], _EXFAT_STATISTICS, fs.exfat_statistics, winioctl/EXFAT_STATISTICS, winioctl/PEXFAT_STATISTICS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - EXFAT_STATISTICS
product: Windows
targetos: Windows
req.typenames: EXFAT_STATISTICS, *PEXFAT_STATISTICS
req.redist: 
---

# _EXFAT_STATISTICS structure


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




<a href="https://msdn.microsoft.com/98d293e8-e708-48f5-99b1-603f27e6ef16">FAT_STATISTICS</a>



<a href="https://msdn.microsoft.com/ff8c7dfe-da7f-4ee2-9a54-613e0cd3e1e2">FILESYSTEM_STATISTICS</a>
 

 

