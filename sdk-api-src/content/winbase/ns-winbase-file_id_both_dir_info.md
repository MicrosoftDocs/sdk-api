---
UID: NS:winbase._FILE_ID_BOTH_DIR_INFO
title: FILE_ID_BOTH_DIR_INFO (winbase.h)
description: Contains information about files in the specified directory.
helpviewer_keywords: ["*PFILE_ID_BOTH_DIR_INFO","FILE_ATTRIBUTE_ARCHIVE","FILE_ATTRIBUTE_COMPRESSED","FILE_ATTRIBUTE_DIRECTORY","FILE_ATTRIBUTE_HIDDEN","FILE_ATTRIBUTE_NORMAL","FILE_ATTRIBUTE_READONLY","FILE_ATTRIBUTE_SYSTEM","FILE_ATTRIBUTE_TEMPORARY","FILE_ID_BOTH_DIR_INFO","FILE_ID_BOTH_DIR_INFO structure [Files]","PFILE_ID_BOTH_DIR_INFO","PFILE_ID_BOTH_DIR_INFO structure pointer [Files]","fileextd/FILE_ID_BOTH_DIR_INFO","fileextd/PFILE_ID_BOTH_DIR_INFO","fs.file_id_both_dir_info","fs.file_id_both_directory_info","winbase/FILE_ID_BOTH_DIR_INFO","winbase/PFILE_ID_BOTH_DIR_INFO"]
old-location: fs\file_id_both_dir_info.htm
tech.root: fs
ms.assetid: d7011ea4-e70a-4c03-a715-6144ce0c7029
ms.date: 12/05/2018
ms.keywords: '*PFILE_ID_BOTH_DIR_INFO, FILE_ATTRIBUTE_ARCHIVE, FILE_ATTRIBUTE_COMPRESSED, FILE_ATTRIBUTE_DIRECTORY, FILE_ATTRIBUTE_HIDDEN, FILE_ATTRIBUTE_NORMAL, FILE_ATTRIBUTE_READONLY, FILE_ATTRIBUTE_SYSTEM, FILE_ATTRIBUTE_TEMPORARY, FILE_ID_BOTH_DIR_INFO, FILE_ID_BOTH_DIR_INFO structure [Files], PFILE_ID_BOTH_DIR_INFO, PFILE_ID_BOTH_DIR_INFO structure pointer [Files], fileextd/FILE_ID_BOTH_DIR_INFO, fileextd/PFILE_ID_BOTH_DIR_INFO, fs.file_id_both_dir_info, fs.file_id_both_directory_info, winbase/FILE_ID_BOTH_DIR_INFO, winbase/PFILE_ID_BOTH_DIR_INFO'
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
req.typenames: FILE_ID_BOTH_DIR_INFO, *PFILE_ID_BOTH_DIR_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_ID_BOTH_DIR_INFO
 - winbase/_FILE_ID_BOTH_DIR_INFO
 - PFILE_ID_BOTH_DIR_INFO
 - winbase/PFILE_ID_BOTH_DIR_INFO
 - FILE_ID_BOTH_DIR_INFO
 - winbase/FILE_ID_BOTH_DIR_INFO
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
 - FILE_ID_BOTH_DIR_INFO
---

# FILE_ID_BOTH_DIR_INFO structure


## -description

Contains information about files in the specified directory. Used for directory handles. 
   Use only when calling 
   <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>. The number of 
   files that are returned for each call to 
   <b>GetFileInformationByHandleEx</b> depends on the 
   size of the buffer that is passed to the function. Any subsequent calls to 
   <b>GetFileInformationByHandleEx</b> on the same 
   handle will resume the enumeration operation after the last file is returned.

## -struct-fields

### -field NextEntryOffset

The offset for the next <b>FILE_ID_BOTH_DIR_INFO</b> 
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

The absolute new end-of-file position as a byte offset from the start of the file to the end of the file. 
      Because this value is zero-based, it actually refers to the first free byte in the file. In other words, 
      <b>EndOfFile</b> is the offset to the byte that immediately follows the last valid byte in 
      the file.

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

### -field ShortNameLength

The length of <b>ShortName</b>.

### -field ShortName

The short 8.3 file naming convention (for example, 
      "FILENAME.TXT") name of the file.

### -field FileId

The file ID.

### -field FileName

The first character of the file name string. This is followed in memory by the remainder of the 
      string.

## -remarks

No specific access rights are required to query this information.

File reference numbers, also called file IDs, are guaranteed to be unique only within a static file system. 
    They are not guaranteed to be unique over time, because file systems are free to reuse them. Nor are they 
    guaranteed to remain constant. For example, the FAT file system generates the file reference number for a file 
    from the byte offset of the file's directory entry record (DIRENT) on the disk. Defragmentation can change this 
    byte offset. Thus a FAT file reference number can change over time.

All dates and times are in absolute system-time format. Absolute system time is the number of 100-nanosecond 
    intervals since the start of the year 1601.

This <b>FILE_ID_BOTH_DIR_INFO</b> structure must be 
    aligned on a <b>DWORDLONG</b> (8-byte) boundary. If a buffer contains two or more of these structures, the 
    <b>NextEntryOffset</b> value in each entry, except the last, falls on an 8-byte boundary.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>