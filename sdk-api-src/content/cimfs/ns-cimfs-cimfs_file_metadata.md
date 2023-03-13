---
UID: NS:cimfs._CIMFS_FILE_METADATA
title: CIMFS_FILE_METADATA
description: The CIMFS_FILE_METADATA structure specifies file metadata for the file to be added by CimCreateFile.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: _CIMFS_FILE_METADATA, CIMFS_FILE_METADATA
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: cimfs.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: CIMFS_FILE_METADATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - cimfs.h
api_name:
 - _CIMFS_FILE_METADATA
 - CIMFS_FILE_METADATA
f1_keywords:
 - _CIMFS_FILE_METADATA
 - cimfs/_CIMFS_FILE_METADATA
 - CIMFS_FILE_METADATA
 - cimfs/CIMFS_FILE_METADATA
---

## -description

Structure that specifies file metadata for the file to be added by CimCreateFile.

## -struct-fields

### -field Attributes

File attributes

### -field FileSize

Size of the file. The file can be written up to this size by CimWriteFile.

### -field CreationTime

Creation time

### -field LastWriteTime

Last write time

### -field ChangeTime

Change time

### -field LastAccessTime

Last access time

### -field SecurityDescriptorBuffer

Buffer containing the file security descriptor 

### -field SecurityDescriptorSize

Size of the security descriptor buffer in bytes

### -field ReparseDataBuffer

Buffer containing the file reparse data

### -field ReparseDataSize

Size of the ReparseDataBuffer in bytes

### -field EaBuffer

Buffer containing a FILE_FULL_EA_INFORMATION structure for the file extended attributes

### -field EaBufferSize

Size of the EaBuffer in bytes

## -remarks

## -see-also
