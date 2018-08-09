---
UID: NS:fileapi._WIN32_FILE_ATTRIBUTE_DATA
title: "_WIN32_FILE_ATTRIBUTE_DATA"
author: windows-sdk-content
description: Contains attribute information for a file or directory.
old-location: fs\win32_file_attribute_data_str.htm
old-project: fileio
ms.assetid: e1a7fb5c-2d69-40e3-b9d8-b583a03d828a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPWIN32_FILE_ATTRIBUTE_DATA, LPWIN32_FILE_ATTRIBUTE_DATA, LPWIN32_FILE_ATTRIBUTE_DATA structure pointer [Files], WIN32_FILE_ATTRIBUTE_DATA, WIN32_FILE_ATTRIBUTE_DATA structure [Files], _WIN32_FILE_ATTRIBUTE_DATA, _win32_win32_file_attribute_data_str, base.win32_file_attribute_data_str, fileapi/LPWIN32_FILE_ATTRIBUTE_DATA, fileapi/WIN32_FILE_ATTRIBUTE_DATA, fs.win32_file_attribute_data_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WIN32_FILE_ATTRIBUTE_DATA, *LPWIN32_FILE_ATTRIBUTE_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fileapi.h
api_name:
 - WIN32_FILE_ATTRIBUTE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# _WIN32_FILE_ATTRIBUTE_DATA structure


## -description


Contains attribute information for a file or directory. The 
    <a href="https://msdn.microsoft.com/e5d84000-17c1-4517-97a7-6bd240d73814">GetFileAttributesEx</a> function uses this 
    structure.


## -struct-fields




### -field dwFileAttributes

The file system attribute information for a file or directory.
      

For possible values and their descriptions, see <a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>.


### -field ftCreationTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that specifies when the file or 
      directory is created.
      

If the underlying file system does not support creation time, this member is zero.


### -field ftLastAccessTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.
      

For a file, the structure specifies when the file is last read from or written to.

For a directory, the structure specifies when the directory is created.

For both files and directories, the specified date is correct, but the time of day is always set to midnight. 
       If the underlying file system does not support last access time, this member is zero.


### -field ftLastWriteTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.
      

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
    <a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>.




## -see-also




<a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>



<a href="https://msdn.microsoft.com/e5d84000-17c1-4517-97a7-6bd240d73814">GetFileAttributesEx</a>
 

 

