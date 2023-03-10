---
UID: NS:winioctl._FILE_MAKE_COMPATIBLE_BUFFER
title: FILE_MAKE_COMPATIBLE_BUFFER
description: Specifies the disc to close the current session for. This control code is used for UDF file systems. This structure is used for input when calling FSCTL_MAKE_MEDIA_COMPATIBLE.
helpviewer_keywords: ["*PFILE_MAKE_COMPATIBLE_BUFFER","FILE_MAKE_COMPATIBLE_BUFFER","FILE_MAKE_COMPATIBLE_BUFFER structure [Files]","PFILE_MAKE_COMPATIBLE_BUFFER","PFILE_MAKE_COMPATIBLE_BUFFER structure pointer [Files]","fs.file_make_compatible_buffer","winioctl/FILE_MAKE_COMPATIBLE_BUFFER","winioctl/PFILE_MAKE_COMPATIBLE_BUFFER"]
old-location: fs\file_make_compatible_buffer.htm
tech.root: fs
ms.assetid: 1c7b1958-099f-404d-a060-99efc543a3c0
ms.date: 12/05/2018
ms.keywords: '*PFILE_MAKE_COMPATIBLE_BUFFER, FILE_MAKE_COMPATIBLE_BUFFER, FILE_MAKE_COMPATIBLE_BUFFER structure [Files], PFILE_MAKE_COMPATIBLE_BUFFER, PFILE_MAKE_COMPATIBLE_BUFFER structure pointer [Files], fs.file_make_compatible_buffer, winioctl/FILE_MAKE_COMPATIBLE_BUFFER, winioctl/PFILE_MAKE_COMPATIBLE_BUFFER'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FILE_MAKE_COMPATIBLE_BUFFER, *PFILE_MAKE_COMPATIBLE_BUFFER
req.redist: 
f1_keywords:
 - _FILE_MAKE_COMPATIBLE_BUFFER
 - winioctl/_FILE_MAKE_COMPATIBLE_BUFFER
 - PFILE_MAKE_COMPATIBLE_BUFFER
 - winioctl/PFILE_MAKE_COMPATIBLE_BUFFER
 - FILE_MAKE_COMPATIBLE_BUFFER
 - winioctl/FILE_MAKE_COMPATIBLE_BUFFER
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
 - FILE_MAKE_COMPATIBLE_BUFFER
---

# FILE_MAKE_COMPATIBLE_BUFFER structure


## -description

Specifies the disc to close the current session for. This control code is used for UDF file systems. This structure is used for input when calling <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_make_media_compatible">FSCTL_MAKE_MEDIA_COMPATIBLE</a>.

## -struct-fields

### -field CloseDisc

If <b>TRUE</b>, indicates the media should be finalized. No new data can be appended to the media.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_make_media_compatible">FSCTL_MAKE_MEDIA_COMPATIBLE</a>