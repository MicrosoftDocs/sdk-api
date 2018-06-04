---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

