---
UID: NS:winioctl._NTFS_STATISTICS_EX
title: NTFS_STATISTICS_EX
description: Contains statistical information from the NTFS file system.Support for this structure started with Windows 10.
helpviewer_keywords: ["*PNTFS_STATISTICS_EX","NTFS_STATISTICS_EX","NTFS_STATISTICS_EX structure [Files]","PNTFS_STATISTICS_EX","PNTFS_STATISTICS_EX structure pointer [Files]","fs.ntfs_statistics_ex","winioctl/NTFS_STATISTICS_EX","winioctl/PNTFS_STATISTICS_EX"]
old-location: fs\ntfs_statistics_ex.htm
tech.root: fs
ms.assetid: D1A6995C-A4BA-4ECC-892A-196581FA41CE
ms.date: 12/05/2018
ms.keywords: '*PNTFS_STATISTICS_EX, NTFS_STATISTICS_EX, NTFS_STATISTICS_EX structure [Files], PNTFS_STATISTICS_EX, PNTFS_STATISTICS_EX structure pointer [Files], fs.ntfs_statistics_ex, winioctl/NTFS_STATISTICS_EX, winioctl/PNTFS_STATISTICS_EX'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: NTFS_STATISTICS_EX, *PNTFS_STATISTICS_EX
req.redist: 
f1_keywords:
 - _NTFS_STATISTICS_EX
 - winioctl/_NTFS_STATISTICS_EX
 - PNTFS_STATISTICS_EX
 - winioctl/PNTFS_STATISTICS_EX
 - NTFS_STATISTICS_EX
 - winioctl/NTFS_STATISTICS_EX
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
 - NTFS_STATISTICS_EX
---

# NTFS_STATISTICS_EX structure


## -description



Contains statistical information from the NTFS file system.Support for this structure started with Windows 10.

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

### -field BitmapWritesUserLevel.Flush

The number of bitmap writes due to a flush operation.

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

### -field Allocate.RunsReturned

The number of runs used to satisfy all the requests.

### -field Allocate.Hints

The number of times a hint was specified.

### -field Allocate.HintsHonored

The number of times the hint was useful.

### -field Allocate.Cache

The number of times the cache was useful other than the hint.

### -field Allocate.CacheMiss

The number of times the cache was not useful.

### -field Allocate.Clusters

The number of clusters allocated.

### -field Allocate.HintsClusters

The number of clusters allocated through the hint.

### -field Allocate.CacheClusters

The number of clusters allocated through the cache other than the hint.

### -field Allocate.CacheMissClusters

The number of clusters allocated without the cache.

### -field DiskResourcesExhausted

The number of failed attempts made to acquire a slab of storage for use on the current thinly provisioned volume.

### -field VolumeTrimCount

The number of volume level trim operations issued.

### -field VolumeTrimTime

The total time elapsed during all volume level trim operations.  This value, divided by the frequency value from <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency">QueryPerformanceFrequency</a> or <a href="/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter">KeQueryPerformanceCounter</a>,  will give the time in seconds.

### -field VolumeTrimByteCount

The total number of bytes issued by all volume level trim operations.

### -field FileLevelTrimCount

The number of file level trim operations issued.

### -field FileLevelTrimTime

The total time elapsed during all file level trim operations. This value, divided by the frequency value from <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency">QueryPerformanceFrequency</a> or <a href="/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter">KeQueryPerformanceCounter</a>, will give the time in seconds.

### -field FileLevelTrimByteCount

The total number of bytes issued by all file level trim operations.

### -field VolumeTrimSkippedCount

The number of times a volume level trim operation was aborted before being sent down through the storage stack.

### -field VolumeTrimSkippedByteCount

The number of bytes  that were not sent through a volume level trim operation because they were skipped.

### -field NtfsFillStatInfoFromMftRecordCalledCount

### -field NtfsFillStatInfoFromMftRecordBailedBecauseOfAttributeListCount

### -field NtfsFillStatInfoFromMftRecordBailedBecauseOfNonResReparsePointCount

## -remarks

The MFT, MFT mirror, root index, user index, bitmap, and MFT bitmap are counted as metadata files. The log 
    file is not counted as a metadata file.

The number of read and write operations measured is the number of paging operations.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-filesystem_statistics">FILESYSTEM_STATISTICS</a>



<a href="/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter">KeQueryPerformanceCounter</a>



<a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency">QueryPerformanceFrequency</a>
