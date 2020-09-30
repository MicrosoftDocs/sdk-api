---
UID: NS:winioctl._FILE_ALLOCATED_RANGE_BUFFER
title: FILE_ALLOCATED_RANGE_BUFFER
description: Indicates a range of bytes in a file.
helpviewer_keywords: ["*PFILE_ALLOCATED_RANGE_BUFFER","FILE_ALLOCATED_RANGE_BUFFER","FILE_ALLOCATED_RANGE_BUFFER structure [Files]","PFILE_ALLOCATED_RANGE_BUFFER","PFILE_ALLOCATED_RANGE_BUFFER structure pointer [Files]","_win32_file_allocated_range_buffer_str","base.file_allocated_range_buffer_str","fs.file_allocated_range_buffer_str","winioctl/FILE_ALLOCATED_RANGE_BUFFER","winioctl/PFILE_ALLOCATED_RANGE_BUFFER"]
old-location: fs\file_allocated_range_buffer_str.htm
tech.root: fs
ms.assetid: e9c7d757-df29-4419-baba-56beb41623bf
ms.date: 12/05/2018
ms.keywords: '*PFILE_ALLOCATED_RANGE_BUFFER, FILE_ALLOCATED_RANGE_BUFFER, FILE_ALLOCATED_RANGE_BUFFER structure [Files], PFILE_ALLOCATED_RANGE_BUFFER, PFILE_ALLOCATED_RANGE_BUFFER structure pointer [Files], _win32_file_allocated_range_buffer_str, base.file_allocated_range_buffer_str, fs.file_allocated_range_buffer_str, winioctl/FILE_ALLOCATED_RANGE_BUFFER, winioctl/PFILE_ALLOCATED_RANGE_BUFFER'
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
req.typenames: FILE_ALLOCATED_RANGE_BUFFER, *PFILE_ALLOCATED_RANGE_BUFFER
req.redist: 
f1_keywords:
 - _FILE_ALLOCATED_RANGE_BUFFER
 - winioctl/_FILE_ALLOCATED_RANGE_BUFFER
 - PFILE_ALLOCATED_RANGE_BUFFER
 - winioctl/PFILE_ALLOCATED_RANGE_BUFFER
 - FILE_ALLOCATED_RANGE_BUFFER
 - winioctl/FILE_ALLOCATED_RANGE_BUFFER
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
 - FILE_ALLOCATED_RANGE_BUFFER
---

# FILE_ALLOCATED_RANGE_BUFFER structure


## -description

Indicates a range of bytes in a file. This structure is used with the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges">FSCTL_QUERY_ALLOCATED_RANGES</a> control code. On input, the structure indicates the range of the file to search. On output, the operation retrieves an array of 
<b>FILE_ALLOCATED_RANGE_BUFFER</b> structures to indicate the allocated ranges within the search range.

## -struct-fields

### -field FileOffset

The file offset of the start of a range of bytes in a file, in bytes.

### -field Length

The size of the range, in bytes.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges">FSCTL_QUERY_ALLOCATED_RANGES</a>



<a href="/windows/desktop/FileIO/sparse-files">Sparse Files</a>