---
UID: NS:winioctl._NTFS_STATISTICS
title: NTFS_STATISTICS
description: Contains statistical information from the NTFS file system.
helpviewer_keywords: ["*PNTFS_STATISTICS","NTFS_STATISTICS","NTFS_STATISTICS structure [Files]","PNTFS_STATISTICS","PNTFS_STATISTICS structure pointer [Files]","base.ntfs_statistics_str","fs.ntfs_statistics_str","winioctl/NTFS_STATISTICS","winioctl/PNTFS_STATISTICS"]
old-location: fs\ntfs_statistics_str.htm
tech.root: fs
ms.assetid: 9b5cffc5-386d-4333-9a37-cc27b8f9b187
ms.date: 12/05/2018
ms.keywords: '*PNTFS_STATISTICS, NTFS_STATISTICS, NTFS_STATISTICS structure [Files], PNTFS_STATISTICS, PNTFS_STATISTICS structure pointer [Files], base.ntfs_statistics_str, fs.ntfs_statistics_str, winioctl/NTFS_STATISTICS, winioctl/PNTFS_STATISTICS'
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
req.typenames: NTFS_STATISTICS, *PNTFS_STATISTICS
req.redist: 
f1_keywords:
 - _NTFS_STATISTICS
 - winioctl/_NTFS_STATISTICS
 - PNTFS_STATISTICS
 - winioctl/PNTFS_STATISTICS
 - NTFS_STATISTICS
 - winioctl/NTFS_STATISTICS
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
 - NTFS_STATISTICS
---

# NTFS_STATISTICS structure


## -description

Contains statistical information from the NTFS file system.
<div class="alert"><b>Tip</b>  Applications targeting Windows 10 can access additional statistics through <a href="/windows/desktop/api/winioctl/ns-winioctl-ntfs_statistics_ex">NTFS_STATISTICS_EX</a>.  </div><div> </div>

## -struct-fields

### -field LogFileFullExceptions

The number of exceptions generated due to the log file being full.

### -field OtherExceptions

The number of other exceptions generated.

### -field MftReads

The number of read operations on the master file table (MFT).

### -field MftReadBytes

The number of bytes read from the MFT.

### -field MftWrites

The number of write operations on the MFT.

### -field MftWriteBytes

The number of bytes written to the MFT.

### -field MftWritesUserLevel

### -field MftWritesUserLevel.Write

The number of MFT writes due to a write operation.

### -field MftWritesUserLevel.Create

The number of MFT writes due to a create operation.

### -field MftWritesUserLevel.SetInfo

The number of MFT writes due to setting file information.

### -field MftWritesUserLevel.Flush

The number of MFT writes due to a flush operation.

### -field MftWritesFlushForLogFileFull

The number of flushes of the MFT performed because the log file was full.

### -field MftWritesLazyWriter

The number of MFT write operations performed by the lazy writer thread.

### -field MftWritesUserRequest

Reserved.

### -field Mft2Writes

The number of write operations on the MFT mirror.

### -field Mft2WriteBytes

The number of bytes written to the MFT mirror.

### -field Mft2WritesUserLevel

### -field Mft2WritesUserLevel.Write

The number of MFT mirror writes due to a write operation.

### -field Mft2WritesUserLevel.Create

The number of MFT mirror writes due to a create operation.

### -field Mft2WritesUserLevel.SetInfo

The number of MFT mirror writes due to setting file information.

### -field Mft2WritesUserLevel.Flush

The number of MFT mirror writes due to a flush operation.

### -field Mft2WritesFlushForLogFileFull

The number of flushes of the MFT mirror performed because the log file was full.

### -field Mft2WritesLazyWriter

The number of MFT mirror write operations performed by the lazy writer thread.

### -field Mft2WritesUserRequest

Reserved.

### -field RootIndexReads

The number of read operations on the root index.

### -field RootIndexReadBytes

The number of bytes read from the root index.

### -field RootIndexWrites

The number of write operations on the root index.

### -field RootIndexWriteBytes

The number of bytes written to the root index.

### -field BitmapReads

The number of read operations on the cluster allocation bitmap.

### -field BitmapReadBytes

The number of bytes read from the cluster allocation bitmap.

### -field BitmapWrites

The number of write operations on the cluster allocation bitmap.

### -field BitmapWriteBytes

The number of bytes written to the cluster allocation bitmap.

### -field BitmapWritesFlushForLogFileFull

The number of flushes of the bitmap performed because the log file was full.

### -field BitmapWritesLazyWriter

The number of bitmap write operations performed by the lazy writer thread.

### -field BitmapWritesUserRequest

Reserved.

### -field BitmapWritesUserLevel

### -field BitmapWritesUserLevel.Write

The number of bitmap writes due to a write operation.

### -field BitmapWritesUserLevel.Create

The number of bitmap writes due to a create operation.

### -field BitmapWritesUserLevel.SetInfo

The number of bitmap writes due to setting file information.

### -field MftBitmapReads

The number of read operations on the MFT bitmap.

### -field MftBitmapReadBytes

The number of bytes read from the MFT bitmap.

### -field MftBitmapWrites

The number of write operations on the MFT bitmap.

### -field MftBitmapWriteBytes

The number of bytes written to the MFT bitmap.

### -field MftBitmapWritesFlushForLogFileFull

The number of flushes of the MFT bitmap performed because the log file was full.

### -field MftBitmapWritesLazyWriter

The number of MFT bitmap write operations performed by the lazy writer thread.

### -field MftBitmapWritesUserRequest

Reserved.

### -field MftBitmapWritesUserLevel

### -field MftBitmapWritesUserLevel.Write

The number of MFT bitmap writes due to a write operation.

### -field MftBitmapWritesUserLevel.Create

The number of bitmap writes due to a create operation.

### -field MftBitmapWritesUserLevel.SetInfo

The number of bitmap writes due to setting file information.

### -field MftBitmapWritesUserLevel.Flush

The number of bitmap writes due to a flush operation.

### -field UserIndexReads

The number of read operations on the user index.

### -field UserIndexReadBytes

The number of bytes read from the user index.

### -field UserIndexWrites

The number of write operations on the user index.

### -field UserIndexWriteBytes

The number of bytes written to the user index.

### -field LogFileReads

The number of read operations on the log file.

### -field LogFileReadBytes

The number of bytes read from the log file.

### -field LogFileWrites

The number of write operations on the log file.

### -field LogFileWriteBytes

The number of bytes written to the log file.

### -field Allocate

### -field Allocate.Calls

The number of individual calls to allocate clusters.

### -field Allocate.Clusters

The number of clusters allocated.

### -field Allocate.Hints

The number of times a hint was specified.

### -field Allocate.RunsReturned

The number of runs used to satisfy all the requests.

### -field Allocate.HintsHonored

The number of times the hint was useful.

### -field Allocate.HintsClusters

The number of clusters allocated through the hint.

### -field Allocate.Cache

The number of times the cache was useful other than the hint.

### -field Allocate.CacheClusters

The number of clusters allocated through the cache other than the hint.

### -field Allocate.CacheMiss

The number of times the cache was not useful.

### -field Allocate.CacheMissClusters

The number of clusters allocated without the cache.

### -field DiskResourcesExhausted

The number of failed attempts made to acquire a slab of storage for use on the current thinly provisioned volume.

Support for this member started with Windows 8.1.

## -remarks

The MFT, MFT mirror, root index, user index, bitmap, and MFT bitmap are counted as metadata files. The log 
    file is not counted as a metadata file.

The number of read and write operations measured is the number of paging operations.

For additional statistics that are only available with Windows 10, use <a href="/windows/desktop/api/winioctl/ns-winioctl-ntfs_statistics_ex">NTFS_STATISTICS_EX</a>.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-filesystem_statistics">FILESYSTEM_STATISTICS</a>



<a href="/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter">KeQueryPerformanceCounter</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-ntfs_statistics_ex">NTFS_STATISTICS_EX</a>



<a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency">QueryPerformanceFrequency</a>
