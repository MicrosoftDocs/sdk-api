---
UID: NS:winioctl._FILE_LEVEL_TRIM_OUTPUT
title: FILE_LEVEL_TRIM_OUTPUT
description: Used as output to the FSCTL_FILE_LEVEL_TRIM control code.
helpviewer_keywords: ["*PFILE_LEVEL_TRIM_OUTPUT","FILE_LEVEL_TRIM_OUTPUT","FILE_LEVEL_TRIM_OUTPUT structure [Files]","PFILE_LEVEL_TRIM_OUTPUT","PFILE_LEVEL_TRIM_OUTPUT structure pointer [Files]","fs.file_level_trim_output","winioctl/FILE_LEVEL_TRIM_OUTPUT","winioctl/PFILE_LEVEL_TRIM_OUTPUT"]
old-location: fs\file_level_trim_output.htm
tech.root: fs
ms.assetid: 3d293d09-8d41-495d-9095-f2f24bf6ac6b
ms.date: 12/05/2018
ms.keywords: '*PFILE_LEVEL_TRIM_OUTPUT, FILE_LEVEL_TRIM_OUTPUT, FILE_LEVEL_TRIM_OUTPUT structure [Files], PFILE_LEVEL_TRIM_OUTPUT, PFILE_LEVEL_TRIM_OUTPUT structure pointer [Files], fs.file_level_trim_output, winioctl/FILE_LEVEL_TRIM_OUTPUT, winioctl/PFILE_LEVEL_TRIM_OUTPUT'
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
req.typenames: FILE_LEVEL_TRIM_OUTPUT, *PFILE_LEVEL_TRIM_OUTPUT
req.redist: 
f1_keywords:
 - _FILE_LEVEL_TRIM_OUTPUT
 - winioctl/_FILE_LEVEL_TRIM_OUTPUT
 - PFILE_LEVEL_TRIM_OUTPUT
 - winioctl/PFILE_LEVEL_TRIM_OUTPUT
 - FILE_LEVEL_TRIM_OUTPUT
 - winioctl/FILE_LEVEL_TRIM_OUTPUT
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
 - FILE_LEVEL_TRIM_OUTPUT
---

# FILE_LEVEL_TRIM_OUTPUT structure


## -description

Used as output to the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_file_level_trim">FSCTL_FILE_LEVEL_TRIM</a> control code.

## -struct-fields

### -field NumRangesProcessed

Contains the number of ranges that were successfully processed. This may be less than the value passed in 
      the <b>NumRanges</b> member of the 
      <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_file_level_trim">FILE_LEVEL_TRIM</a> structure. If it is then the last 
      ranges in the array were not processed.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_file_level_trim">FSCTL_FILE_LEVEL_TRIM</a>