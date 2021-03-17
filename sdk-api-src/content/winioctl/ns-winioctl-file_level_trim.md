---
UID: NS:winioctl._FILE_LEVEL_TRIM
title: FILE_LEVEL_TRIM
description: Used as input to the FSCTL_FILE_LEVEL_TRIM control code.
helpviewer_keywords: ["*PFILE_LEVEL_TRIM","FILE_LEVEL_TRIM","FILE_LEVEL_TRIM structure [Files]","PFILE_LEVEL_TRIM","PFILE_LEVEL_TRIM structure pointer [Files]","fs.file_level_trim","winioctl/FILE_LEVEL_TRIM","winioctl/PFILE_LEVEL_TRIM"]
old-location: fs\file_level_trim.htm
tech.root: fs
ms.assetid: db3ac916-83e7-4aa1-b5aa-dab139a0a21a
ms.date: 12/05/2018
ms.keywords: '*PFILE_LEVEL_TRIM, FILE_LEVEL_TRIM, FILE_LEVEL_TRIM structure [Files], PFILE_LEVEL_TRIM, PFILE_LEVEL_TRIM structure pointer [Files], fs.file_level_trim, winioctl/FILE_LEVEL_TRIM, winioctl/PFILE_LEVEL_TRIM'
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
req.typenames: FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM
req.redist: 
f1_keywords:
 - _FILE_LEVEL_TRIM
 - winioctl/_FILE_LEVEL_TRIM
 - PFILE_LEVEL_TRIM
 - winioctl/PFILE_LEVEL_TRIM
 - FILE_LEVEL_TRIM
 - winioctl/FILE_LEVEL_TRIM
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
 - FILE_LEVEL_TRIM
---

# FILE_LEVEL_TRIM structure


## -description

Used as input to the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_file_level_trim">FSCTL_FILE_LEVEL_TRIM</a> control code.

## -struct-fields

### -field Key

Reserved. Set to zero (0).

### -field NumRanges

Number of <a href="/windows/desktop/api/winioctl/ns-winioctl-file_level_trim_range">FILE_LEVEL_TRIM_RANGE</a> entries in 
      the <b>Ranges</b> member. On return should be compared with the 
      <b>NumRangesProcessed</b> member of the 
      <a href="/windows/desktop/api/winioctl/ns-winioctl-file_level_trim_output">FILE_LEVEL_TRIM_OUTPUT</a> structure.

### -field Ranges

Array of ranges that describe the portions of the file that are to be trimmed.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-file_level_trim_output">FILE_LEVEL_TRIM_OUTPUT</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-file_level_trim_range">FILE_LEVEL_TRIM_RANGE</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_file_level_trim">FSCTL_FILE_LEVEL_TRIM</a>