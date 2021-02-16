---
UID: NS:winbase._FILE_STREAM_INFO
title: FILE_STREAM_INFO (winbase.h)
description: Receives file stream information for the specified file.
helpviewer_keywords: ["*PFILE_STREAM_INFO","FILE_STREAM_INFO","FILE_STREAM_INFO structure [Files]","PFILE_STREAM_INFO","PFILE_STREAM_INFO structure pointer [Files]","fileextd/FILE_STREAM_INFO","fileextd/PFILE_STREAM_INFO","fs.file_stream_info","winbase/FILE_STREAM_INFO","winbase/PFILE_STREAM_INFO"]
old-location: fs\file_stream_info.htm
tech.root: fs
ms.assetid: 36d1b0b3-bd6b-41e7-937a-4e8deef6f9da
ms.date: 12/05/2018
ms.keywords: '*PFILE_STREAM_INFO, FILE_STREAM_INFO, FILE_STREAM_INFO structure [Files], PFILE_STREAM_INFO, PFILE_STREAM_INFO structure pointer [Files], fileextd/FILE_STREAM_INFO, fileextd/PFILE_STREAM_INFO, fs.file_stream_info, winbase/FILE_STREAM_INFO, winbase/PFILE_STREAM_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: FILE_STREAM_INFO, *PFILE_STREAM_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_STREAM_INFO
 - winbase/_FILE_STREAM_INFO
 - PFILE_STREAM_INFO
 - winbase/PFILE_STREAM_INFO
 - FILE_STREAM_INFO
 - winbase/FILE_STREAM_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - FileExtd.h
api_name:
 - FILE_STREAM_INFO
---

# FILE_STREAM_INFO structure


## -description

Receives  file stream information for the specified file. Used for any handles. Use only when calling <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>.

## -struct-fields

### -field NextEntryOffset

The offset for the next <b>FILE_STREAM_INFO</b> entry that is returned. This member is zero if no other entries follow this one.

### -field StreamNameLength

The length, in bytes, of <b>StreamName</b>.

### -field StreamSize

The size, in bytes,  of the data stream.

### -field StreamAllocationSize

The amount of space that  is allocated for the stream, in bytes.  This value is usually a multiple of the sector or cluster size of the underlying physical device.

### -field StreamName

The stream name.

## -remarks

The <b>FILE_STREAM_INFO</b> structure is used to enumerate the streams for a file.



Support for named data streams is file-system-specific. 



The <b>FILE_STREAM_INFO</b> structure must be aligned on a <b>LONGLONG</b> (8-byte) boundary. If a buffer contains two or more of these structures, the <b>NextEntryOffset</b> value in each entry, except the last, falls on an 8-byte boundary.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>