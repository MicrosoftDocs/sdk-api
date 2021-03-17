---
UID: NS:winioctl._FILE_QUERY_ON_DISK_VOL_INFO_BUFFER
title: FILE_QUERY_ON_DISK_VOL_INFO_BUFFER
description: Receives the volume information from a call to FSCTL_QUERY_ON_DISK_VOLUME_INFO.
helpviewer_keywords: ["*PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER","FILE_QUERY_ON_DISK_VOL_INFO_BUFFER","FILE_QUERY_ON_DISK_VOL_INFO_BUFFER structure [Files]","PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER","PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER structure pointer [Files]","fs.file_query_on_disk_vol_info_buffer","winioctl/FILE_QUERY_ON_DISK_VOL_INFO_BUFFER","winioctl/PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER"]
old-location: fs\file_query_on_disk_vol_info_buffer.htm
tech.root: fs
ms.assetid: 812c8840-5e69-4a85-ad93-3be5bf09b917
ms.date: 12/05/2018
ms.keywords: '*PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER, FILE_QUERY_ON_DISK_VOL_INFO_BUFFER, FILE_QUERY_ON_DISK_VOL_INFO_BUFFER structure [Files], PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER, PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER structure pointer [Files], fs.file_query_on_disk_vol_info_buffer, winioctl/FILE_QUERY_ON_DISK_VOL_INFO_BUFFER, winioctl/PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: FILE_QUERY_ON_DISK_VOL_INFO_BUFFER, *PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER
req.redist: 
f1_keywords:
 - _FILE_QUERY_ON_DISK_VOL_INFO_BUFFER
 - winioctl/_FILE_QUERY_ON_DISK_VOL_INFO_BUFFER
 - PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER
 - winioctl/PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER
 - FILE_QUERY_ON_DISK_VOL_INFO_BUFFER
 - winioctl/FILE_QUERY_ON_DISK_VOL_INFO_BUFFER
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
 - FILE_QUERY_ON_DISK_VOL_INFO_BUFFER
---

# FILE_QUERY_ON_DISK_VOL_INFO_BUFFER structure


## -description

Receives the volume information from a call to  <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info">FSCTL_QUERY_ON_DISK_VOLUME_INFO</a>.

## -struct-fields

### -field DirectoryCount

The number of directories on the specified disk. This member is -1 if the number is unknown. 

For UDF file systems with a virtual allocation table, this information is available only if the UDF revision is greater than 1.50.

### -field FileCount

The number of files on the specified disk. Returns -1 if the number is unknown.

For UDF file systems with a virtual allocation table, this information is available only if the UDF revision is greater than 1.50.

### -field FsFormatMajVersion

The major version number of the file system. Returns -1 if the number is unknown or not applicable. On UDF 1.02 file systems, 1 is returned.

### -field FsFormatMinVersion

The minor version number of the file system. Returns -1 if the number is unknown or not applicable.  On UDF 1.02 file systems, 02 is returned.

### -field FsFormatName

Always returns UDF.

### -field FormatTime

The time the media was formatted.

### -field LastUpdateTime

The time the media was last updated.

### -field CopyrightInfo

Any copyright information associated with the volume.

### -field AbstractInfo

Any abstract  information written on the media.

### -field FormattingImplementationInfo

Implementation-specific information; in some cases, it is the operating system version that  the media was formatted by.

### -field LastModifyingImplementationInfo

The last implementation that modified the disk. This information is implementation specific; in some cases, it is the operating system version that  the media was last modified by.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info">FSCTL_QUERY_ON_DISK_VOLUME_INFO</a>