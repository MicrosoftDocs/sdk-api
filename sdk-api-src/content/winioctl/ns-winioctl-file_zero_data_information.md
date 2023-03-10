---
UID: NS:winioctl._FILE_ZERO_DATA_INFORMATION
title: FILE_ZERO_DATA_INFORMATION
description: Contains a range of a file to set to zeros.
helpviewer_keywords: ["*PFILE_ZERO_DATA_INFORMATION","FILE_ZERO_DATA_INFORMATION","FILE_ZERO_DATA_INFORMATION structure [Files]","PFILE_ZERO_DATA_INFORMATION","PFILE_ZERO_DATA_INFORMATION structure pointer [Files]","_win32_file_zero_data_information_str","base.file_zero_data_information_str","fs.file_zero_data_information_str","winioctl/FILE_ZERO_DATA_INFORMATION","winioctl/PFILE_ZERO_DATA_INFORMATION"]
old-location: fs\file_zero_data_information_str.htm
tech.root: fs
ms.assetid: ad2c4e2d-7f41-45e8-beff-2f6d735f152e
ms.date: 12/05/2018
ms.keywords: '*PFILE_ZERO_DATA_INFORMATION, FILE_ZERO_DATA_INFORMATION, FILE_ZERO_DATA_INFORMATION structure [Files], PFILE_ZERO_DATA_INFORMATION, PFILE_ZERO_DATA_INFORMATION structure pointer [Files], _win32_file_zero_data_information_str, base.file_zero_data_information_str, fs.file_zero_data_information_str, winioctl/FILE_ZERO_DATA_INFORMATION, winioctl/PFILE_ZERO_DATA_INFORMATION'
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
req.typenames: FILE_ZERO_DATA_INFORMATION, *PFILE_ZERO_DATA_INFORMATION
req.redist: 
f1_keywords:
 - _FILE_ZERO_DATA_INFORMATION
 - winioctl/_FILE_ZERO_DATA_INFORMATION
 - PFILE_ZERO_DATA_INFORMATION
 - winioctl/PFILE_ZERO_DATA_INFORMATION
 - FILE_ZERO_DATA_INFORMATION
 - winioctl/FILE_ZERO_DATA_INFORMATION
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
 - FILE_ZERO_DATA_INFORMATION
---

# FILE_ZERO_DATA_INFORMATION structure


## -description

Contains a range of a file to set to zeros. This structure is used by the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_zero_data">FSCTL_SET_ZERO_DATA</a> control code

## -struct-fields

### -field FileOffset

The file offset of the start of the range to set to zeros, in bytes.

### -field BeyondFinalZero

The byte offset of the first byte beyond the last zeroed byte.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_zero_data">FSCTL_SET_ZERO_DATA</a>



<a href="/windows/desktop/FileIO/sparse-files">Sparse Files</a>