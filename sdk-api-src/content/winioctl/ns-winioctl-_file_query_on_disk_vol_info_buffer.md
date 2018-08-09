---
UID: NS:winioctl._FILE_QUERY_ON_DISK_VOL_INFO_BUFFER
title: "_FILE_QUERY_ON_DISK_VOL_INFO_BUFFER"
author: windows-sdk-content
description: Receives the volume information from a call to FSCTL_QUERY_ON_DISK_VOLUME_INFO.
old-location: fs\file_query_on_disk_vol_info_buffer.htm
old-project: fileio
ms.assetid: 812c8840-5e69-4a85-ad93-3be5bf09b917
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER, FILE_QUERY_ON_DISK_VOL_INFO_BUFFER, FILE_QUERY_ON_DISK_VOL_INFO_BUFFER structure [Files], PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER, PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER structure pointer [Files], _FILE_QUERY_ON_DISK_VOL_INFO_BUFFER, fs.file_query_on_disk_vol_info_buffer, winioctl/FILE_QUERY_ON_DISK_VOL_INFO_BUFFER, winioctl/PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: FILE_QUERY_ON_DISK_VOL_INFO_BUFFER, *PFILE_QUERY_ON_DISK_VOL_INFO_BUFFER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FILE_QUERY_ON_DISK_VOL_INFO_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_QUERY_ON_DISK_VOL_INFO_BUFFER structure


## -description


Receives the volume information from a call to  <a href="https://msdn.microsoft.com/6d34007e-4e6f-433e-9d85-9b2743e1c1d2">FSCTL_QUERY_ON_DISK_VOLUME_INFO</a>.


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




<a href="https://msdn.microsoft.com/6d34007e-4e6f-433e-9d85-9b2743e1c1d2">FSCTL_QUERY_ON_DISK_VOLUME_INFO</a>
 

 

