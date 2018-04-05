---
UID: NS:minwinbase._WIN32_FIND_DATAA
title: "_WIN32_FIND_DATAA"
author: windows-driver-content
description: Contains information about the file that is found by the FindFirstFile, FindFirstFileEx, or FindNextFile function.
old-location: fs\win32_find_data_str.htm
old-project: FileIO
ms.assetid: eb700d84-0ba5-4af8-a619-2d2544560dbc
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*LPWIN32_FIND_DATAA, *PWIN32_FIND_DATAA, IO_REPARSE_TAG_CSV, IO_REPARSE_TAG_DEDUP, IO_REPARSE_TAG_DFS, IO_REPARSE_TAG_DFSR, IO_REPARSE_TAG_HSM, IO_REPARSE_TAG_HSM2, IO_REPARSE_TAG_MOUNT_POINT, IO_REPARSE_TAG_NFS, IO_REPARSE_TAG_SIS, IO_REPARSE_TAG_SYMLINK, IO_REPARSE_TAG_WIM, LPWIN32_FIND_DATA, LPWIN32_FIND_DATA structure pointer [Files], PWIN32_FIND_DATA, PWIN32_FIND_DATA structure pointer [Files], WIN32_FIND_DATA, WIN32_FIND_DATA structure [Files], WIN32_FIND_DATAA, WIN32_FIND_DATAW, _WIN32_FIND_DATAA, _win32_win32_find_data_str, base.win32_find_data_str, fs.win32_find_data_str, minwinbase/LPWIN32_FIND_DATA, minwinbase/PWIN32_FIND_DATA, minwinbase/WIN32_FIND_DATA, minwinbase/WIN32_FIND_DATAA, minwinbase/WIN32_FIND_DATAW, winbase/LPWIN32_FIND_DATA, winbase/PWIN32_FIND_DATA, winbase/WIN32_FIND_DATA, winbase/WIN32_FIND_DATAA, winbase/WIN32_FIND_DATAW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: minwinbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WIN32_FIND_DATAW (Unicode) and WIN32_FIND_DATAA (ANSI)
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIN32_FIND_DATAA, *PWIN32_FIND_DATAA, *LPWIN32_FIND_DATAA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	MinWinBase.h
-	WinBase.h
api_name:
-	WIN32_FIND_DATA
-	WIN32_FIND_DATAA
-	WIN32_FIND_DATAW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _WIN32_FIND_DATAA structure


## -description


Contains information about the file  that is found by the 
    <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>, 
    <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>, or 
    <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a> function.


## -struct-fields




### -field dwFileAttributes

The file attributes of a file.

For possible values and their descriptions, see 
       <a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>.

The <b>FILE_ATTRIBUTE_SPARSE_FILE</b> attribute on the file is set if any of the streams 
       of the file have ever been sparse.


### -field ftCreationTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that specifies when a file or 
       directory was created.

If the underlying file system does not support creation time, this member is zero.


### -field ftLastAccessTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.

For a file, the structure specifies when the file was last read from, written to, or for executable files, 
       run.

For a directory, the structure specifies when the directory is created. If the underlying file system does 
       not support last access time, this member is zero.

On the FAT file system, the specified date for both files and directories is correct, but the time of day is 
       always set to midnight.


### -field ftLastWriteTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.

For a file, the structure specifies when the file was last written to, truncated, or overwritten, for 
       example, when <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> or 
       <a href="https://msdn.microsoft.com/2a579609-144a-4b77-8605-87aecf1f0957">SetEndOfFile</a> are used. The date and time are not 
       updated when file attributes or security descriptors are changed.

For a directory, the structure specifies when the directory is created. If the underlying file system does 
       not support last write time, this member is zero.


### -field nFileSizeHigh

The high-order <b>DWORD</b> value of the file size, in bytes.

This value is zero unless the file size is greater than <b>MAXDWORD</b>.

The size of the file is equal to (<b>nFileSizeHigh</b> * 
       (<b>MAXDWORD</b>+1)) + <b>nFileSizeLow</b>.


### -field nFileSizeLow

The low-order <b>DWORD</b> value of the file size, in bytes.


### -field dwReserved0

If the <b>dwFileAttributes</b> member includes the 
       <b>FILE_ATTRIBUTE_REPARSE_POINT</b> attribute, this member specifies the reparse point 
       tag.

Otherwise, this value is undefined and should not be used.

For more information see <a href="https://msdn.microsoft.com/d02a2f50-d374-4149-bc04-49b7db052f62">Reparse Point Tags</a>.



#### IO_REPARSE_TAG_CSV (0x80000009)



#### IO_REPARSE_TAG_DEDUP (0x80000013)



#### IO_REPARSE_TAG_DFS (0x8000000A)



#### IO_REPARSE_TAG_DFSR (0x80000012)



#### IO_REPARSE_TAG_HSM (0xC0000004)



#### IO_REPARSE_TAG_HSM2 (0x80000006)



#### IO_REPARSE_TAG_MOUNT_POINT (0xA0000003)



#### IO_REPARSE_TAG_NFS (0x80000014)



#### IO_REPARSE_TAG_SIS (0x80000007)



#### IO_REPARSE_TAG_SYMLINK (0xA000000C)



#### IO_REPARSE_TAG_WIM (0x80000008)


### -field dwReserved1

Reserved for future use.


### -field cFileName

The name of the file.


### -field cAlternateFileName

An alternative name for the file.

This name is in the classic 8.3 file name format.


### -field dwFileType

 


### -field dwCreatorType

 


### -field wFinderFlags

 




## -remarks



If a file has a long file name, the complete name appears in the <b>cFileName</b> member, 
    and the 8.3 format truncated version of the name appears in the <b>cAlternateFileName</b> 
    member. Otherwise, <b>cAlternateFileName</b> is empty. If the 
    <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function was called with a value of 
    <b>FindExInfoBasic</b> in the <i>fInfoLevelId</i> parameter, the 
    <b>cAlternateFileName</b> member will always contain a <b>NULL</b> string 
    value. This remains true for all subsequent calls to the 
    <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a> function. As an alternative method of 
    retrieving the 8.3 format version of a file name, you can use the 
    <a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a> function. For more information about 
    file names, see <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">File Names, Paths, and Namespaces</a>.

Not all file systems can record creation and last access times, and not all file systems record them in the 
    same manner. For example, on the FAT file system, create time has a resolution of 10 milliseconds, write time has 
    a resolution of 2 seconds, and access time has a resolution of 1 day. The 
    NTFS file system delays updates to the last access time for a file by up to 1 hour after the last access. For 
    more information, see <a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>



<a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">File Names, Paths, and Namespaces</a>



<a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>



<a href="https://msdn.microsoft.com/58dfce16-2d7f-4db5-9f84-5dd651d26745">FileTimeToLocalFileTime</a>



<a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a>



<a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>



<a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>



<a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>



<a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a>
 

 

