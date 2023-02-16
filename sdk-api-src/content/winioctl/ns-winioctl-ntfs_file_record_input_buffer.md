---
UID: NS:winioctl.NTFS_FILE_RECORD_INPUT_BUFFER
title: NTFS_FILE_RECORD_INPUT_BUFFER
description: Contains data for the FSCTL_GET_NTFS_FILE_RECORD control code.
helpviewer_keywords: ["*PNTFS_FILE_RECORD_INPUT_BUFFER","NTFS_FILE_RECORD_INPUT_BUFFER","NTFS_FILE_RECORD_INPUT_BUFFER structure [Files]","PNTFS_FILE_RECORD_INPUT_BUFFER","PNTFS_FILE_RECORD_INPUT_BUFFER structure pointer [Files]","_win32_ntfs_file_record_input_buffer_str","base.ntfs_file_record_input_buffer_str","fs.ntfs_file_record_input_buffer_str","winioctl/NTFS_FILE_RECORD_INPUT_BUFFER","winioctl/PNTFS_FILE_RECORD_INPUT_BUFFER"]
old-location: fs\ntfs_file_record_input_buffer_str.htm
tech.root: fs
ms.assetid: 8b0317ca-6d0e-4a04-a05a-1627d22171e3
ms.date: 12/05/2018
ms.keywords: '*PNTFS_FILE_RECORD_INPUT_BUFFER, NTFS_FILE_RECORD_INPUT_BUFFER, NTFS_FILE_RECORD_INPUT_BUFFER structure [Files], PNTFS_FILE_RECORD_INPUT_BUFFER, PNTFS_FILE_RECORD_INPUT_BUFFER structure pointer [Files], _win32_ntfs_file_record_input_buffer_str, base.ntfs_file_record_input_buffer_str, fs.ntfs_file_record_input_buffer_str, winioctl/NTFS_FILE_RECORD_INPUT_BUFFER, winioctl/PNTFS_FILE_RECORD_INPUT_BUFFER'
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
req.typenames: NTFS_FILE_RECORD_INPUT_BUFFER, *PNTFS_FILE_RECORD_INPUT_BUFFER
req.redist: 
f1_keywords:
 - PNTFS_FILE_RECORD_INPUT_BUFFER
 - winioctl/PNTFS_FILE_RECORD_INPUT_BUFFER
 - NTFS_FILE_RECORD_INPUT_BUFFER
 - winioctl/NTFS_FILE_RECORD_INPUT_BUFFER
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
 - NTFS_FILE_RECORD_INPUT_BUFFER
---

# NTFS_FILE_RECORD_INPUT_BUFFER structure


## -description

Contains data for the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record">FSCTL_GET_NTFS_FILE_RECORD</a> control code.

## -struct-fields

### -field FileReferenceNumber

The file identifier of the file record to be retrieved. This is not necessarily the file identifier returned in the <b>FileReferenceNumber</b> member of the 
<a href="/windows/desktop/api/winioctl/ns-winioctl-ntfs_file_record_output_buffer">NTFS_FILE_RECORD_OUTPUT_BUFFER</a> structure. Refer to the Remarks section of the reference page for 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record">FSCTL_GET_NTFS_FILE_RECORD</a> for more information.

## -remarks

Pass this structure as input to the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record">FSCTL_GET_NTFS_FILE_RECORD</a> control code.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record">FSCTL_GET_NTFS_FILE_RECORD</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-ntfs_file_record_output_buffer">NTFS_FILE_RECORD_OUTPUT_BUFFER</a>

