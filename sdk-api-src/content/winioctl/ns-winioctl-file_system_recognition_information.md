---
UID: NS:winioctl._FILE_SYSTEM_RECOGNITION_INFORMATION
title: FILE_SYSTEM_RECOGNITION_INFORMATION
description: Contains file system recognition information retrieved by the FSCTL_QUERY_FILE_SYSTEM_RECOGNITION control code.
helpviewer_keywords: ["*PFILE_SYSTEM_RECOGNITION_INFORMATION","FILE_SYSTEM_RECOGNITION_INFORMATION","FILE_SYSTEM_RECOGNITION_INFORMATION structure [Files]","PFILE_SYSTEM_RECOGNITION_INFORMATION","PFILE_SYSTEM_RECOGNITION_INFORMATION structure pointer [Files]","fs.file_system_recognition_information","winioctl/FILE_SYSTEM_RECOGNITION_INFORMATION","winioctl/PFILE_SYSTEM_RECOGNITION_INFORMATION"]
old-location: fs\file_system_recognition_information.htm
tech.root: fs
ms.assetid: 27d9fd2b-d4c6-4237-8c15-0fa97b63b991
ms.date: 12/05/2018
ms.keywords: '*PFILE_SYSTEM_RECOGNITION_INFORMATION, FILE_SYSTEM_RECOGNITION_INFORMATION, FILE_SYSTEM_RECOGNITION_INFORMATION structure [Files], PFILE_SYSTEM_RECOGNITION_INFORMATION, PFILE_SYSTEM_RECOGNITION_INFORMATION structure pointer [Files], fs.file_system_recognition_information, winioctl/FILE_SYSTEM_RECOGNITION_INFORMATION, winioctl/PFILE_SYSTEM_RECOGNITION_INFORMATION'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: FILE_SYSTEM_RECOGNITION_INFORMATION, *PFILE_SYSTEM_RECOGNITION_INFORMATION
req.redist: 
f1_keywords:
 - _FILE_SYSTEM_RECOGNITION_INFORMATION
 - winioctl/_FILE_SYSTEM_RECOGNITION_INFORMATION
 - PFILE_SYSTEM_RECOGNITION_INFORMATION
 - winioctl/PFILE_SYSTEM_RECOGNITION_INFORMATION
 - FILE_SYSTEM_RECOGNITION_INFORMATION
 - winioctl/FILE_SYSTEM_RECOGNITION_INFORMATION
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
 - FILE_SYSTEM_RECOGNITION_INFORMATION
---

# FILE_SYSTEM_RECOGNITION_INFORMATION structure


## -description

Contains file system recognition information retrieved by the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition">FSCTL_QUERY_FILE_SYSTEM_RECOGNITION</a> control code.

## -struct-fields

### -field FileSystem

The file system name stored on the disk. This is a null-terminated string of 8 ASCII characters that represents the nonlocalizable human-readable name of the 
    file system the volume is formatted with.

## -see-also

<a href="/windows/desktop/FileIO/file-system-recognition-structure">FILE_SYSTEM_RECOGNITION_STRUCTURE</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition">FSCTL_QUERY_FILE_SYSTEM_RECOGNITION</a>