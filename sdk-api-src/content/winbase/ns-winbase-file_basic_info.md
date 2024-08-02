---
UID: NS:winbase._FILE_BASIC_INFO
title: FILE_BASIC_INFO (winbase.h)
description: Contains the basic information for a file. Used for file handles.
helpviewer_keywords: ["*PFILE_BASIC_INFO","FILE_BASIC_INFO","FILE_BASIC_INFO structure [Files]","PFILE_BASIC_INFO","PFILE_BASIC_INFO structure pointer [Files]","fileextd/FILE_BASIC_INFO","fileextd/PFILE_BASIC_INFO","fs.file_basic_info","winbase/FILE_BASIC_INFO","winbase/PFILE_BASIC_INFO"]
old-location: fs\file_basic_info.htm
tech.root: fs
ms.assetid: 7765e430-cf6b-4ccf-b5e7-9fb6e15ca6d6
ms.date: 08/02/2024
ms.keywords: '*PFILE_BASIC_INFO, FILE_BASIC_INFO, FILE_BASIC_INFO structure [Files], PFILE_BASIC_INFO, PFILE_BASIC_INFO structure pointer [Files], fileextd/FILE_BASIC_INFO, fileextd/PFILE_BASIC_INFO, fs.file_basic_info, winbase/FILE_BASIC_INFO, winbase/PFILE_BASIC_INFO'
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
req.typenames: FILE_BASIC_INFO, *PFILE_BASIC_INFO
req.redist: Windows SDK on     Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_BASIC_INFO
 - winbase/_FILE_BASIC_INFO
 - PFILE_BASIC_INFO
 - winbase/PFILE_BASIC_INFO
 - FILE_BASIC_INFO
 - winbase/FILE_BASIC_INFO
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
 - FILE_BASIC_INFO
---

## -description

Contains the basic information for a file. Used for file handles.

## -struct-fields

### -field CreationTime

The time the file was created in <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> format, 
      which is a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (UTC).

### -field LastAccessTime

The time the file was last accessed in <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> 
      format.

### -field LastWriteTime

The time the file was last written to in <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> 
      format.

### -field ChangeTime

The time the file was changed in <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> 
      format.

> [!NOTE]
> The distinction between *ChangeTime* and *LastWriteTime*, is that *LastWriteTime* relates to the underlying data-stream, while *ChangeTime* refers to changes to file metadata, such as renames and attribute changes.

### -field FileAttributes

The file attributes. For a list of attributes, see 
      <a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>. If this is set 
      to 0 in a <b>FILE_BASIC_INFO</b> structure passed to 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a> then none of the 
      attributes are changed.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>
