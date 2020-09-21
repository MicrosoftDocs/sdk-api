---
UID: NS:fileapi._BY_HANDLE_FILE_INFORMATION
title: BY_HANDLE_FILE_INFORMATION (fileapi.h)
description: Contains information that the GetFileInformationByHandle function retrieves.
helpviewer_keywords: ["*LPBY_HANDLE_FILE_INFORMATION","*PBY_HANDLE_FILE_INFORMATION","BY_HANDLE_FILE_INFORMATION","BY_HANDLE_FILE_INFORMATION structure [Files]","LPBY_HANDLE_FILE_INFORMATION","LPBY_HANDLE_FILE_INFORMATION structure pointer [Files]","PBY_HANDLE_FILE_INFORMATION","PBY_HANDLE_FILE_INFORMATION structure pointer [Files]","_win32_by_handle_file_information_str","base.by_handle_file_information_str","fileapi/BY_HANDLE_FILE_INFORMATION","fileapi/LPBY_HANDLE_FILE_INFORMATION","fileapi/PBY_HANDLE_FILE_INFORMATION","fs.by_handle_file_information_str","winbase/BY_HANDLE_FILE_INFORMATION","winbase/LPBY_HANDLE_FILE_INFORMATION","winbase/PBY_HANDLE_FILE_INFORMATION"]
old-location: fs\by_handle_file_information_str.htm
tech.root: fs
ms.assetid: a6fc5cf0-d3b0-4a76-af8b-6a13ab32157d
ms.date: 12/05/2018
ms.keywords: '*LPBY_HANDLE_FILE_INFORMATION, *PBY_HANDLE_FILE_INFORMATION, BY_HANDLE_FILE_INFORMATION, BY_HANDLE_FILE_INFORMATION structure [Files], LPBY_HANDLE_FILE_INFORMATION, LPBY_HANDLE_FILE_INFORMATION structure pointer [Files], PBY_HANDLE_FILE_INFORMATION, PBY_HANDLE_FILE_INFORMATION structure pointer [Files], _win32_by_handle_file_information_str, base.by_handle_file_information_str, fileapi/BY_HANDLE_FILE_INFORMATION, fileapi/LPBY_HANDLE_FILE_INFORMATION, fileapi/PBY_HANDLE_FILE_INFORMATION, fs.by_handle_file_information_str, winbase/BY_HANDLE_FILE_INFORMATION, winbase/LPBY_HANDLE_FILE_INFORMATION, winbase/PBY_HANDLE_FILE_INFORMATION'
req.header: fileapi.h
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
req.typenames: BY_HANDLE_FILE_INFORMATION, *PBY_HANDLE_FILE_INFORMATION, *LPBY_HANDLE_FILE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BY_HANDLE_FILE_INFORMATION
 - fileapi/_BY_HANDLE_FILE_INFORMATION
 - PBY_HANDLE_FILE_INFORMATION
 - fileapi/PBY_HANDLE_FILE_INFORMATION
 - BY_HANDLE_FILE_INFORMATION
 - fileapi/BY_HANDLE_FILE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FileAPI.h
 - WinBase.h
api_name:
 - BY_HANDLE_FILE_INFORMATION
---

# BY_HANDLE_FILE_INFORMATION structure


## -description

Contains information that the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a> function 
    retrieves.

## -struct-fields

### -field dwFileAttributes

The file attributes. For possible values and their descriptions, see 
      <a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>.

### -field ftCreationTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies when a file or 
      directory is created. If the underlying file system does not support creation time, this member is 
      zero (0).

### -field ftLastAccessTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure. For a file, the structure 
     specifies the last time that a file is read from or written to. For a directory, the structure specifies when the 
     directory is created. For both files and directories, the specified date is correct, but the time of day is 
     always set to midnight. If the underlying file system does not support the last access time, this member is 
     zero (0).

### -field ftLastWriteTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure. For a file, the structure 
      specifies the last time that a file is written to. For a directory, the structure specifies when the directory 
      is created. If the underlying file system does not support the last write time, this member is zero (0).

### -field dwVolumeSerialNumber

The serial number of the volume that contains a file.

### -field nFileSizeHigh

The high-order part of the file size.

### -field nFileSizeLow

The low-order part of the file size.

### -field nNumberOfLinks

The number of links to this file. For the FAT file system this member is always 1. For the NTFS file 
      system, it can be more than 1.

### -field nFileIndexHigh

The high-order part of a unique identifier that is associated with a file. For more information, see 
      <b>nFileIndexLow</b>.

### -field nFileIndexLow

The low-order part of a unique identifier that is associated with a file.

The identifier (low and high parts) and the volume serial number uniquely identify a file on a single 
       computer. To determine whether two open handles represent the same file, combine the identifier and the volume 
       serial number for each file and compare them.

The ReFS file system, introduced with Windows Server 2012, includes 128-bit file identifiers. To 
       retrieve the 128-bit file identifier use the 
       <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a> function 
       with <b>FileIdInfo</b> to retrieve the 
       <a href="/windows/desktop/api/winbase/ns-winbase-file_id_info">FILE_ID_INFO</a> structure. The 64-bit identifier in this 
       structure is not guaranteed to be unique on ReFS.

## -remarks

The identifier that is stored in the <b>nFileIndexHigh</b> and 
    <b>nFileIndexLow</b> members is called the file ID. Support for file IDs is file 
    system-specific. File IDs are not guaranteed to be unique over time, because file systems are free to reuse them. 
    In some cases, the file ID for a file can change over time.

In the FAT file system, the file ID is generated from the first cluster of the containing directory and the 
    byte offset within the directory of the entry for the file. Some defragmentation products change this byte offset. 
    (Windows in-box defragmentation does not.) Thus, a FAT file ID can change over time. Renaming a file in the FAT 
    file system can also change the file ID, but only if the new file name is longer than the old one.

In the NTFS file system, a file keeps the same file ID until it is deleted. You can replace one file with 
    another file without changing the file ID by using the 
    <a href="/windows/desktop/api/winbase/nf-winbase-replacefilea">ReplaceFile</a> function. However, the file ID of the 
    replacement file, not the replaced file, is retained as the file ID of the resulting file.

Not all file systems can record creation and last access time, and not all file systems record them in the 
    same manner. For example, on a Windows FAT file system, create time has a resolution of 10 milliseconds, write 
    time has a resolution of 2 seconds, and access time has a resolution of 1 day (the access date). On the NTFS file 
    system, access time has a resolution of 1 hour. For more information, see 
    <a href="/windows/desktop/SysInfo/file-times">File Times</a>.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/winbase/ns-winbase-file_id_info">FILE_ID_INFO</a>



<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>