---
UID: NS:winioctl._FILE_LEVEL_TRIM_RANGE
title: FILE_LEVEL_TRIM_RANGE
description: Specifies a range of a file that is to be trimmed.
helpviewer_keywords: ["*PFILE_LEVEL_TRIM_RANGE","FILE_LEVEL_TRIM_RANGE","FILE_LEVEL_TRIM_RANGE structure [Files]","PFILE_LEVEL_TRIM_RANGE","PFILE_LEVEL_TRIM_RANGE structure pointer [Files]","fs.file_level_trim_range","winioctl/FILE_LEVEL_TRIM_RANGE","winioctl/PFILE_LEVEL_TRIM_RANGE"]
old-location: fs\file_level_trim_range.htm
tech.root: fs
ms.assetid: 2ee14239-68bb-40f6-b10b-2500d316dcc8
ms.date: 12/05/2018
ms.keywords: '*PFILE_LEVEL_TRIM_RANGE, FILE_LEVEL_TRIM_RANGE, FILE_LEVEL_TRIM_RANGE structure [Files], PFILE_LEVEL_TRIM_RANGE, PFILE_LEVEL_TRIM_RANGE structure pointer [Files], fs.file_level_trim_range, winioctl/FILE_LEVEL_TRIM_RANGE, winioctl/PFILE_LEVEL_TRIM_RANGE'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: FILE_LEVEL_TRIM_RANGE, *PFILE_LEVEL_TRIM_RANGE
req.redist: 
f1_keywords:
 - _FILE_LEVEL_TRIM_RANGE
 - winioctl/_FILE_LEVEL_TRIM_RANGE
 - PFILE_LEVEL_TRIM_RANGE
 - winioctl/PFILE_LEVEL_TRIM_RANGE
 - FILE_LEVEL_TRIM_RANGE
 - winioctl/FILE_LEVEL_TRIM_RANGE
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
 - FILE_LEVEL_TRIM_RANGE
---

# FILE_LEVEL_TRIM_RANGE structure


## -description

Specifies a range of a file that is to be trimmed.

## -struct-fields

### -field Offset

Offset, in bytes, from the start of the file for the range to be trimmed.

### -field Length

Length, in bytes, for the range to be trimmed.

## -remarks

Before the trim operation is passed to the underlying storage system the input ranges are reduced to be 
    aligned to page boundaries (4,096 bytes on 32-bit and x64-based editions of Windows, 8,192 bytes on Itanium-Based 
    editions of Windows).

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_file_level_trim">FILE_LEVEL_TRIM</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-file_level_trim_output">FILE_LEVEL_TRIM_OUTPUT</a>



<b>FSCTL_FILE_LEVEL_TRIM</b>