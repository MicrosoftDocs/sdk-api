---
UID: NS:fileapi._WIN32_FILE_ATTRIBUTE_DATA
title: WIN32_FILE_ATTRIBUTE_DATA (fileapi.h)
description: Contains attribute information for a file or directory.
helpviewer_keywords: ["*LPWIN32_FILE_ATTRIBUTE_DATA","LPWIN32_FILE_ATTRIBUTE_DATA","LPWIN32_FILE_ATTRIBUTE_DATA structure pointer [Files]","WIN32_FILE_ATTRIBUTE_DATA","WIN32_FILE_ATTRIBUTE_DATA structure [Files]","_win32_win32_file_attribute_data_str","base.win32_file_attribute_data_str","fileapi/LPWIN32_FILE_ATTRIBUTE_DATA","fileapi/WIN32_FILE_ATTRIBUTE_DATA","fs.win32_file_attribute_data_str"]
old-location: fs\win32_file_attribute_data_str.htm
tech.root: fs
ms.assetid: e1a7fb5c-2d69-40e3-b9d8-b583a03d828a
ms.date: 12/05/2018
ms.keywords: '*LPWIN32_FILE_ATTRIBUTE_DATA, LPWIN32_FILE_ATTRIBUTE_DATA, LPWIN32_FILE_ATTRIBUTE_DATA structure pointer [Files], WIN32_FILE_ATTRIBUTE_DATA, WIN32_FILE_ATTRIBUTE_DATA structure [Files], _win32_win32_file_attribute_data_str, base.win32_file_attribute_data_str, fileapi/LPWIN32_FILE_ATTRIBUTE_DATA, fileapi/WIN32_FILE_ATTRIBUTE_DATA, fs.win32_file_attribute_data_str'
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
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
req.typenames: WIN32_FILE_ATTRIBUTE_DATA, *LPWIN32_FILE_ATTRIBUTE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIN32_FILE_ATTRIBUTE_DATA
 - fileapi/_WIN32_FILE_ATTRIBUTE_DATA
 - LPWIN32_FILE_ATTRIBUTE_DATA
 - fileapi/LPWIN32_FILE_ATTRIBUTE_DATA
 - WIN32_FILE_ATTRIBUTE_DATA
 - fileapi/WIN32_FILE_ATTRIBUTE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fileapi.h
api_name:
 - WIN32_FILE_ATTRIBUTE_DATA
---

# WIN32_FILE_ATTRIBUTE_DATA structure


## -description

Contains attribute information for a file or directory. The 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesexa">GetFileAttributesEx</a> function uses this 
    structure.

## -struct-fields

### -field dwFileAttributes

The file system attribute information for a file or directory.
      

For possible values and their descriptions, see <a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>.

### -field ftCreationTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies when the file or 
      directory is created.
      

If the underlying file system does not support creation time, this member is zero.

### -field ftLastAccessTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.
      

For a file, the structure specifies when the file is last read from or written to.

For a directory, the structure specifies when the directory is created.

For both files and directories, the specified date is correct, but the time of day is always set to midnight. 
       If the underlying file system does not support last access time, this member is zero.

### -field ftLastWriteTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.
      

For a file, the structure specifies when the file is last written to.

For a directory, the structure specifies when the directory is created.

If the underlying file system does not support last write time, this member is zero.

### -field nFileSizeHigh

The high-order 
     <b>DWORD</b> of the file size.
      

This member does not have a meaning for directories.

### -field nFileSizeLow

The low-order <b>DWORD</b> of the file size.
      

This member does not have a meaning for directories.

## -remarks

Not all file systems can record creation and last access time, and not all file systems record them in the 
    same manner. For example, on the FAT file system, create time has a resolution of 10 milliseconds, write time has 
    a resolution of 2 seconds, and access time has a resolution of 1 day. On the NTFS file 
    system, access time has a resolution of 1 hour. For more information, see 
    <a href="/windows/desktop/SysInfo/file-times">File Times</a>.

## -see-also

<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesexa">GetFileAttributesEx</a>