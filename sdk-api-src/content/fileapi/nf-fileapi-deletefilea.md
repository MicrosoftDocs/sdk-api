---
UID: NF:fileapi.DeleteFileA
title: DeleteFileA function (fileapi.h)
description: Deletes an existing file. (DeleteFileA)
helpviewer_keywords: ["DeleteFileA", "fileapi/DeleteFileA"]
old-location: fs\deletefile.htm
tech.root: fs
ms.assetid: 0b947a85-816b-4374-a8f8-c369e366a17d
ms.date: 12/15/2023
ms.keywords: DeleteFile, DeleteFile function [Files], DeleteFileA, DeleteFileW, _win32_deletefile, base.deletefile, fileapi/DeleteFile, fileapi/DeleteFileA, fileapi/DeleteFileW, fs.deletefile, winbase/DeleteFile, winbase/DeleteFileA, winbase/DeleteFileW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteFileW (Unicode) and DeleteFileA (ANSI)
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
 - DeleteFileA
 - fileapi/DeleteFileA
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
 - DeleteFile
 - DeleteFileA
 - DeleteFileW
---

# DeleteFileA function

## -description

Deletes an existing file.

To perform this operation as a transacted operation, use the [DeleteFileTransacted](/windows/win32/api/winbase/nf-winbase-deletefiletransacteda) function.

## -parameters

### -param lpFileName [in]

The name of the file to be deleted.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

If an application attempts to delete a file that does not exist, the **DeleteFile** function fails with **ERROR_FILE_NOT_FOUND**. If the file is a read-only file, the function fails with **ERROR_ACCESS_DENIED**.

The following list identifies some tips for deleting, removing, or closing files:

- To delete a read-only file, first you must remove the read-only attribute.
- To delete or rename a file, you must have either delete permission on the file, or delete child permission in the parent directory.
- To recursively delete the files in a directory, use the [SHFileOperation](/windows/win32/api/shellapi/nf-shellapi-shfileoperationa) function.
- To remove an empty directory, use the [RemoveDirectory](nf-fileapi-removedirectorya.md) function.
- To close an open file, use the [CloseHandle](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.

If you set up a directory with all access except delete and delete child, and the access control lists (ACL) of new files are inherited, then you can create a file without being able to delete it. However, then you can create a file, and then get all the access you request on the handle that is returned to you at the time you create the file.

If you request delete permission at the time you create a file, you can delete or rename the file with that handle, but not with any other handle. For more information, see [File Security and Access Rights](/windows/win32/FileIO/file-security-and-access-rights).

The **DeleteFile** function fails if an application attempts to delete a file that has other handles open for normal I/O or as a memory-mapped file (**FILE_SHARE_DELETE** must have been specified when other handles were opened).

The **DeleteFile** function marks a file for deletion on close. Therefore, the file deletion does not occur until the last handle to the file is closed. Subsequent calls to [CreateFile](nf-fileapi-createfilea.md) to open the file fail with **ERROR_ACCESS_DENIED**.

The use of POSIX delete causes the file to be deleted while handles remain open. Subsequent calls to [CreateFile](nf-fileapi-createfilea.md) to open the file fail with **ERROR_FILE_NOT_FOUND**.

Symbolic link behavior:

If the path points to a symbolic link, the symbolic link is deleted, not the target. To delete a target, you must call [CreateFile](nf-fileapi-createfilea.md) and specify **FILE_FLAG_DELETE_ON_CLOSE**.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies:

| Technology | Supported |
|------------|-----------|
| Server Message Block (SMB) 3.0 protocol | Yes |
| SMB 3.0 Transparent Failover (TFO) | Yes |
| SMB 3.0 with Scale-out File Shares (SO) | Yes |
| Cluster Shared Volume File System (CsvFS) | Yes |
| Resilient File System (ReFS) | Yes |

#### Examples

For an example, see [Locking and Unlocking Byte Ranges in Files](/windows/win32/FileIO/locking-and-unlocking-byte-ranges-in-files).

> [!NOTE]
> The fileapi.h header defines **DeleteFile** as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[CloseHandle](/windows/win32/api/handleapi/nf-handleapi-closehandle)

[CreateFile](nf-fileapi-createfilea.md)

[DeleteFileTransacted](/windows/win32/api/winbase/nf-winbase-deletefiletransacteda)

[File Management Functions](/windows/win32/FileIO/file-management-functions)

[Symbolic Links](/windows/win32/FileIO/symbolic-links)
