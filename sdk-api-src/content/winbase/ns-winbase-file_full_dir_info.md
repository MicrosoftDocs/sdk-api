---
UID: NS:winbase._FILE_FULL_DIR_INFO
title: FILE_FULL_DIR_INFO (winbase.h)
description: Contains directory information for a file. (FILE_FULL_DIR_INFO)
helpviewer_keywords: ["*PFILE_FULL_DIR_INFO","FILE_ATTRIBUTE_ARCHIVE","FILE_ATTRIBUTE_COMPRESSED","FILE_ATTRIBUTE_DIRECTORY","FILE_ATTRIBUTE_HIDDEN","FILE_ATTRIBUTE_NORMAL","FILE_ATTRIBUTE_READONLY","FILE_ATTRIBUTE_SYSTEM","FILE_ATTRIBUTE_TEMPORARY","FILE_FULL_DIR_INFO","FILE_FULL_DIR_INFO structure [Files]","PFILE_FULL_DIR_INFO","PFILE_FULL_DIR_INFO structure pointer [Files]","_FILE_FULL_DIR_INFO","fs.file_full_dir_info","winbase/FILE_FULL_DIR_INFO","winbase/PFILE_FULL_DIR_INFO"]
old-location: fs\file_full_dir_info.htm
tech.root: fs
ms.assetid: 606726e7-fd6b-4419-bd37-7282283007f8
ms.date: 12/05/2018
ms.keywords: '*PFILE_FULL_DIR_INFO, FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_COMPRESSED, FILE_ATTRIBUTE_DIRECTORY, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, FILE_FULL_DIR_INFO, FILE_FULL_DIR_INFO structure [Files], PFILE_FULL_DIR_INFO, PFILE_FULL_DIR_INFO structure pointer [Files], _FILE_FULL_DIR_INFO, fs.file_full_dir_info, winbase/FILE_FULL_DIR_INFO, winbase/PFILE_FULL_DIR_INFO'
req.header: winbase.h
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
req.typenames: FILE_FULL_DIR_INFO, *PFILE_FULL_DIR_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILE_FULL_DIR_INFO
 - winbase/_FILE_FULL_DIR_INFO
 - PFILE_FULL_DIR_INFO
 - winbase/PFILE_FULL_DIR_INFO
 - FILE_FULL_DIR_INFO
 - winbase/FILE_FULL_DIR_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - FILE_FULL_DIR_INFO
---

# FILE_FULL_DIR_INFO structure


## -description

Contains directory information for a file. This structure is returned from the 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a> function when 
    <b>FileFullDirectoryInfo</b> or <b>FileFullDirectoryRestartInfo</b> is 
    passed in the <i>FileInformationClass</i> parameter.

## -struct-fields

### -field NextEntryOffset

The offset for the next <b>FILE_FULL_DIR_INFO</b> 
      structure that is returned. Contains zero (0) if no other entries follow this one.

### -field FileIndex

The byte offset of the file within the parent directory. This member is undefined for file systems, such as 
      NTFS, in which the position of a file within the parent directory is not fixed and can be changed at any time to 
      maintain sort order.

### -field CreationTime

The time that the file was created.

### -field LastAccessTime

The time that the file was last accessed.

### -field LastWriteTime

The time that the file was last written to.

### -field ChangeTime

The time that the file was last changed.

### -field EndOfFile

The absolute new end-of-file position as a byte offset from the start of the file to the end of the default 
      data stream of the file. Because this value is zero-based, it actually refers to the first free byte in the 
      file. In other words, <b>EndOfFile</b> is the offset to the byte that immediately follows 
      the last valid byte in the file.

### -field AllocationSize

The number of bytes that are allocated for the file. This value is usually a multiple of the sector or 
      cluster size of the underlying physical device.

### -field FileAttributes

The file attributes. This member can be any valid combination of the following attributes:



#### FILE_ATTRIBUTE_ARCHIVE (0x00000020)



#### FILE_ATTRIBUTE_COMPRESSED (0x00000800)



#### FILE_ATTRIBUTE_DIRECTORY (0x00000010)



#### FILE_ATTRIBUTE_HIDDEN (0x00000002)



#### FILE_ATTRIBUTE_NORMAL (0x00000080)



#### FILE_ATTRIBUTE_READONLY (0x00000001)



#### FILE_ATTRIBUTE_SYSTEM (0x00000004)



#### FILE_ATTRIBUTE_TEMPORARY (0x00000100)

### -field FileNameLength

The length of the file name.

### -field EaSize

The size of the extended attributes for the file.

### -field FileName

The first character of the file name string. This is followed in memory by the remainder of the 
      string.

## -remarks

The <b>FILE_FULL_DIR_INFO</b> structure is a subset of the 
    information in the <a href="/windows/desktop/api/winbase/ns-winbase-file_id_both_dir_info">FILE_ID_BOTH_DIR_INFO</a> structure. 
    If the additional information is not needed then the operation will be faster as it comes from the directory 
    entry; <b>FILE_ID_BOTH_DIR_INFO</b> contains information 
    from both the directory entry and the Master File Table (MFT).

No specific access rights are required to 
    query this information.

All dates and times are in absolute system-time format. Absolute system time is the number of 100-nanosecond 
    intervals since the start of the year 1601.

This <b>FILE_FULL_DIR_INFO</b> structure must be aligned 
    on a <b>LONGLONG</b> (8-byte) boundary. If a buffer contains two or more of these 
    structures, the <b>NextEntryOffset</b> value in each entry, except the last, falls on an 
    8-byte boundary.

To compile an application that uses this structure, define the <b>_WIN32_WINNT</b> macro 
    as 0x0600 or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>
