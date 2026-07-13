---
UID: NF:fileapi.GetVolumeInformationA
title: GetVolumeInformationA function (fileapi.h)
description: Retrieves information about the file system and volume associated with the specified root directory. (ANSI)
helpviewer_keywords: ["FILE_CASE_PRESERVED_NAMES", "FILE_CASE_SENSITIVE_SEARCH", "FILE_DAX_VOLUME", "FILE_FILE_COMPRESSION", "FILE_NAMED_STREAMS", "FILE_PERSISTENT_ACLS", "FILE_READ_ONLY_VOLUME", "FILE_SEQUENTIAL_WRITE_ONCE", "FILE_SUPPORTS_ENCRYPTION", "FILE_SUPPORTS_EXTENDED_ATTRIBUTES", "FILE_SUPPORTS_HARD_LINKS", "FILE_SUPPORTS_OBJECT_IDS", "FILE_SUPPORTS_OPEN_BY_FILE_ID", "FILE_SUPPORTS_REPARSE_POINTS", "FILE_SUPPORTS_SPARSE_FILES", "FILE_SUPPORTS_TRANSACTIONS", "FILE_SUPPORTS_USN_JOURNAL", "FILE_UNICODE_ON_DISK", "FILE_VOLUME_IS_COMPRESSED", "FILE_VOLUME_QUOTAS", "GetVolumeInformationA", "fileapi/GetVolumeInformationA"]
old-location: fs\getvolumeinformation.htm
tech.root: fs
ms.assetid: c80a38e1-319e-4f15-8c8a-9d29075e1709
ms.date: 01/08/2025
ms.keywords: FILE_CASE_PRESERVED_NAMES, FILE_CASE_SENSITIVE_SEARCH, FILE_DAX_VOLUME, FILE_FILE_COMPRESSION, FILE_NAMED_STREAMS, FILE_PERSISTENT_ACLS, FILE_READ_ONLY_VOLUME, FILE_SEQUENTIAL_WRITE_ONCE, FILE_SUPPORTS_ENCRYPTION, FILE_SUPPORTS_EXTENDED_ATTRIBUTES, FILE_SUPPORTS_HARD_LINKS, FILE_SUPPORTS_OBJECT_IDS, FILE_SUPPORTS_OPEN_BY_FILE_ID, FILE_SUPPORTS_REPARSE_POINTS, FILE_SUPPORTS_SPARSE_FILES, FILE_SUPPORTS_TRANSACTIONS, FILE_SUPPORTS_USN_JOURNAL, FILE_UNICODE_ON_DISK, FILE_VOLUME_IS_COMPRESSED, FILE_VOLUME_QUOTAS, GetVolumeInformation, GetVolumeInformation function [Files], GetVolumeInformationA, GetVolumeInformationW, _win32_getvolumeinformation, base.getvolumeinformation, fileapi/GetVolumeInformation, fileapi/GetVolumeInformationA, fileapi/GetVolumeInformationW, fs.getvolumeinformation, winbase/GetVolumeInformation, winbase/GetVolumeInformationA, winbase/GetVolumeInformationW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi: GetVolumeInformationW (Unicode) and GetVolumeInformationA (ANSI)
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
 - GetVolumeInformationA
 - fileapi/GetVolumeInformationA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetVolumeInformation
 - GetVolumeInformationA
 - GetVolumeInformationW
---

# GetVolumeInformationA function

## -description

Retrieves information about the file system and volume associated with the specified root
    directory.

To specify a handle when retrieving this information, use the [GetVolumeInformationByHandleW](nf-fileapi-getvolumeinformationbyhandlew.md) function.

To retrieve the current compression state of a file or directory, use [FSCTL_GET_COMPRESSION](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression).

## -parameters

### -param lpRootPathName [in, optional]

A pointer to a string that contains the root directory of the volume to be described.

If this parameter is **NULL**, the root of the current directory is used. A trailing backslash is required. For example, you  specify \\\\MyServer\\MyShare as "\\\\MyServer\\MyShare\\", or the C drive as "C:\\".

### -param lpVolumeNameBuffer [out, optional]

A pointer to a buffer that receives the name of a specified volume. The buffer size is specified by the _nVolumeNameSize_ parameter.

### -param nVolumeNameSize [in]

The length of a volume name buffer, in **TCHARs**. The maximum buffer size is **MAX_PATH**+1.

This parameter is ignored if the volume name buffer is not supplied.

### -param lpVolumeSerialNumber [out, optional]

A pointer to a variable that receives the volume serial number.

This parameter can be **NULL** if the serial number is not required.

This function returns the volume serial number that the operating system assigns when a hard disk is formatted. To programmatically obtain the hard disk's serial number that the manufacturer assigns, use the Windows Management Instrumentation (WMI) [Win32_PhysicalMedia](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) property **SerialNumber**.

### -param lpMaximumComponentLength [out, optional]

A pointer to a variable that receives the maximum length, in **TCHARs**, of a file name component  that a specified file system supports.

A file name component is the portion of a file name between backslashes.

The value that is stored in the variable that *_lpMaximumComponentLength_ points to is used to indicate that a specified file system supports long names. For example, for a FAT file system that supports long names, the function stores the value 255, rather than the previous 8.3 indicator. Long names can also be supported on systems that use the NTFS file system.

### -param lpFileSystemFlags [out, optional]

A pointer to a variable that receives flags associated with the specified file system.

This parameter can be one or more of the following flags. However, **FILE_FILE_COMPRESSION** and **FILE_VOL_IS_COMPRESSED** are mutually exclusive.

| Value | Meaning |
|--------|--------|
| **FILE_CASE_SENSITIVE_SEARCH**<br/>0x00000001 | The specified volume supports case-sensitive file names. |
| **FILE_CASE_PRESERVED_NAMES**<br/>0x00000002 | The specified volume supports preserved case of file names when it places a name on disk. |
| **FILE_UNICODE_ON_DISK**<br/>0x00000004 | The specified volume supports Unicode in file names as they appear on disk. |
| **FILE_PERSISTENT_ACLS**<br/>0x00000008 | The specified volume preserves and enforces access control lists (ACL). For example, the NTFS file system preserves and enforces ACLs, and the FAT file system does not. |
| **FILE_FILE_COMPRESSION**<br/>0x00000010 | The specified volume supports file-based compression. |
| **FILE_VOLUME_QUOTAS**<br/>0x00000020 | The specified volume supports disk quotas. |
| **FILE_SUPPORTS_SPARSE_FILES**<br/>0x00000040 | The specified volume supports sparse files. |
| **FILE_SUPPORTS_REPARSE_POINTS**<br/>0x00000080 | The specified volume supports reparse points.<br/><br/>**ReFS:** ReFS supports reparse points but does not index them so [FindFirstVolumeMountPoint](/windows/win32/api/winbase/nf-winbase-findfirstvolumemountpointa) and [FindNextVolumeMountPoint](/windows/win32/api/winbase/nf-winbase-findnextvolumemountpointa) will not function as expected. |
| **FILE_SUPPORTS_REMOTE_STORAGE**<br/>0x00000100 | The file system supports remote storage. |
| **FILE_RETURNS_CLEANUP_RESULT_INFO**<br/>0x00000200 | On a successful cleanup operation, the file system returns information that describes additional actions taken during cleanup, such as deleting the file. File system filters can examine this information in their post-cleanup callback. |
| **FILE_SUPPORTS_POSIX_UNLINK_RENAME**<br/>0x00000400 | The file system supports POSIX-style delete and rename operations. |
| **FILE_VOLUME_IS_COMPRESSED**<br/>0x00008000 | The specified volume is a compressed volume, for example, a DoubleSpace volume. |
| **FILE_SUPPORTS_OBJECT_IDS**<br/>0x00010000 | The specified volume supports object identifiers. |
| **FILE_SUPPORTS_ENCRYPTION**<br/>0x00020000 | The specified volume supports the Encrypted File System (EFS). For more information, see [File Encryption](/windows/win32/FileIO/file-encryption). |
| **FILE_NAMED_STREAMS**<br/>0x00040000 | The specified volume supports named streams. |
| **FILE_READ_ONLY_VOLUME**<br/>0x00080000 | The specified volume is read-only. |
| **FILE_SEQUENTIAL_WRITE_ONCE**<br/>0x00100000 | The specified volume supports a single sequential write. |
| **FILE_SUPPORTS_TRANSACTIONS**<br/>0x00200000 | The specified volume supports transactions. For more information, see [About KTM](/windows/win32/Ktm/about-ktm). |
| **FILE_SUPPORTS_HARD_LINKS**<br/>0x00400000 | The specified volume supports hard links. For more information, see [Hard Links and Junctions](/windows/win32/FileIO/hard-links-and-junctions).<br/><br/>**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7. |
| **FILE_SUPPORTS_EXTENDED_ATTRIBUTES**<br/>0x00800000 | The specified volume supports extended attributes. An extended attribute is a piece of application-specific metadata that an application can associate with a file and is not part of the file's data.<br/><br/>**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7. |
| **FILE_SUPPORTS_OPEN_BY_FILE_ID**<br/>0x01000000 | The file system supports open by FileID. For more information, see [FILE_ID_BOTH_DIR_INFO](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info).<br/><br/>**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7. |
| **FILE_SUPPORTS_USN_JOURNAL**<br/>0x02000000 | The specified volume supports update sequence number (USN) journals. For more information, see [Change Journal Records](/windows/win32/FileIO/change-journal-records).<br/><br/>**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7. |
| **FILE_SUPPORTS_INTEGRITY_STREAMS**<br/>0x04000000 | The file system supports [integrity streams](/windows-server/storage/refs/integrity-streams). |
| **FILE_SUPPORTS_BLOCK_REFCOUNTING**<br/>0x08000000 | The specified volume supports sharing logical clusters between files on the same volume. The file system reallocates on writes to shared clusters. Indicates that **FSCTL_DUPLICATE_EXTENTS_TO_FILE** is a supported operation. |
| **FILE_SUPPORTS_SPARSE_VDL**<br/>0x10000000 | The file system tracks whether each cluster of a file contains valid data (either from explicit file writes or automatic zeros) or invalid data (has not yet been written to or zeroed). File systems that use sparse valid data length (VDL) do not store a valid data length and do not require that valid data be contiguous within a file. |
| **FILE_DAX_VOLUME**<br/>0x20000000 | The specified volume is a direct access (DAX) volume.<br/><br/><b>Note:</b><br/>This flag was introduced in Windows 10, version 1607. |
| **FILE_SUPPORTS_GHOSTING**<br/>0x40000000 | The file system supports ghosting. |

### -param lpFileSystemNameBuffer [out, optional]

A pointer to a buffer that receives the name of the file system, for example, the FAT file system or the NTFS file system. The buffer size is specified by the _nFileSystemNameSize_ parameter.

### -param nFileSystemNameSize [in]

The length of the file system name buffer, in **TCHARs**. The maximum buffer size is **MAX_PATH**+1.

This parameter is ignored if the file system name buffer is not supplied.

## -returns

If all the requested information is retrieved, the return value is nonzero.

If not all the requested information is retrieved, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

When a user attempts to get information about a floppy drive that does not have a floppy disk, or a CD-ROM drive that does not have a compact disc, the system displays a message box for the user to insert a floppy disk or a compact disc, respectively. To prevent the system from displaying this message box, call the [SetErrorMode](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with **SEM_FAILCRITICALERRORS**.

The **FILE_VOL_IS_COMPRESSED** flag is the only indicator of volume-based compression. The file system name is not altered to indicate compression, for example, this flag is returned set on a DoubleSpace volume. When compression is volume-based, an entire volume is  compressed or not compressed.

The **FILE_FILE_COMPRESSION** flag indicates whether a file system supports file-based compression. When compression is file-based, individual files can be compressed or not compressed.

The **FILE_FILE_COMPRESSION** and **FILE_VOL_IS_COMPRESSED** flags are mutually exclusive. Both bits cannot be returned set.

The maximum component length value that is stored in _lpMaximumComponentLength_ is the only indicator that a volume supports longer-than-normal FAT file system (or other file system) file names. The file system name is not altered to indicate support for long file names.

The [GetCompressedFileSize](nf-fileapi-getcompressedfilesizea.md) function obtains the compressed size of a file. The [GetFileAttributes](nf-fileapi-getfileattributesa.md) function can determine whether an individual file is compressed.

#### Symbolic link behavior

If the path points to a symbolic link, the function returns volume information for the target.

Starting with Windows 8 and Windows Server 2012, this function is supported by the following technologies.

| Technology | Supported |
|--------|--------|
| Server Message Block (SMB) 3.0 protocol | No |
| SMB 3.0 Transparent Failover (TFO) | No |
| SMB 3.0 with Scale-out File Shares (SO) | No |
| Cluster Shared Volume File System (CsvFS) | Yes |
| Resilient File System (ReFS) | Yes |

SMB does not support volume management functions.

#### Transacted Operations

If the volume supports file system transactions, the function returns **FILE_SUPPORTS_TRANSACTIONS** in _lpFileSystemFlags_.

> [!NOTE]
> The fileapi.h header defines GetVolumeInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[About KTM](/windows/win32/Ktm/about-ktm)

[File Encryption](/windows/win32/FileIO/file-encryption)

[GetCompressedFileSize](nf-fileapi-getcompressedfilesizea.md)

[GetFileAttributes](nf-fileapi-getfileattributesa.md)

[GetVolumeInformationByHandleW](nf-fileapi-getvolumeinformationbyhandlew.md)

[SetErrorMode](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)

[SetVolumeLabel](/windows/win32/api/winbase/nf-winbase-setvolumelabela)

[Volume Management Functions](/windows/win32/FileIO/volume-management-functions)
