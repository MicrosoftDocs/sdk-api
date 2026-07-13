---
UID: NF:fileapi.DeleteFile2W
tech.root: fs
title: DeleteFile2W function (fileapi.h)
ms.date: 04/10/2025
targetos: Windows
description: Deletes an existing file. (Unicode)
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: fileapi.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 24H2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2025 [desktop apps \| UWP apps]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - fileapi.h
api_name:
 - DeleteFile2W
 - DeleteFile2
f1_keywords:
 - DeleteFile2W
 - fileapi/DeleteFile2W
 - DeleteFile2
 - fileapi/DeleteFile2
dev_langs:
 - c++
helpviewer_keywords:
 - DeleteFile2W
---

## -description

Deletes an existing file.

To perform this operation as a transacted operation, use the [DeleteFileTransacted](../winbase/nf-winbase-deletefiletransactedw.md) function.

## -parameters

### -param lpFileName

The name of the file to be deleted.

By default, the name is limited to **MAX_PATH** characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> You can opt-in to remove the **MAX_PATH** limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param Flags

Flags to specify how to treat the file that is being deleted. This parameter can be a combination one the following values:

| Value | Meaning |
|-------|-------------|
| **FILE_FLAG_DISALLOW_PATH_REDIRECTS**<br/>`0x00010000` | Prevent *lpFileName* from being redirected by reparse points or symbolic links. |

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (`0`). To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md). Possible errors include the following:

| Return code | Description |
|-------------|-------------|
| **ERROR_PATH_REDIRECTED** | *lpFileName* was redirected by reparse points and/or symbolic links. |

## -remarks

If an application attempts to delete a file that does not exist, the **DeleteFile2** function fails with **ERROR_FILE_NOT_FOUND**. If the file is a read-only file, the function fails with **ERROR_ACCESS_DENIED**.

The following list identifies some tips for deleting, removing, or closing files:

- To delete a read-only file, first you must remove the read-only attribute.
- To delete or rename a file, you must have either delete permission on the file, or delete child permission in the parent directory.
- To recursively delete the files in a directory, use the [SHFileOperation](../shellapi/nf-shellapi-shfileoperationw.md) function.
- To remove an empty directory, use the [RemoveDirectory](nf-fileapi-removedirectoryw.md) function.
- To close an open file, use the [CloseHandle](../handleapi/nf-handleapi-closehandle.md) function.

If you set up a directory with all access except delete and delete child, and the access control lists (ACL) of new files are inherited, then you can create a file without being able to delete it. However, then you can create a file, and then get all the access you request on the handle that is returned to you at the time you create the file.

If you request delete permission at the time you create a file, you can delete or rename the file with that handle, but not with any other handle. For more information, see [File Security and Access Rights](/windows/win32/FileIO/file-security-and-access-rights).

The **DeleteFile2** function fails if an application attempts to delete a file that has other handles open for normal I/O or as a memory-mapped file (**FILE_SHARE_DELETE** must have been specified when other handles were opened).

The **DeleteFile2** function marks a file for deletion on close. Therefore, the file deletion does not occur until the last handle to the file is closed. Subsequent calls to [CreateFile](nf-fileapi-createfilew.md), [CreateFile2](nf-fileapi-createfile2.md), or [CreateFile3](nf-fileapi-createfile3.md) to open the file fail with **ERROR_ACCESS_DENIED**.

The use of POSIX delete causes the file to be deleted while handles remain open. Subsequent calls to [CreateFile](nf-fileapi-createfilew.md) to open the file fail with **ERROR_FILE_NOT_FOUND**.

#### Symbolic link behavior

If the path points to a symbolic link, the symbolic link is deleted, not the target. To delete a target, you must call [CreateFile](nf-fileapi-createfilew.md) and specify **FILE_FLAG_DELETE_ON_CLOSE**.

This function is supported by the following technologies:

| Technology | Supported |
|------------|-----------|
| Server Message Block (SMB) 3.0 protocol | Yes |
| SMB 3.0 Transparent Failover (TFO) | Yes |
| SMB 3.0 with Scale-out File Shares (SO) | Yes |
| Cluster Shared Volume File System (CsvFS) | Yes |
| Resilient File System (ReFS) | Yes |

> [!NOTE]
> The `fileapi.h` header defines **DeleteFile2** as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

#### Examples

For an example, see [Locking and Unlocking Byte Ranges in Files](/windows/win32/fileio/locking-and-unlocking-byte-ranges-in-files).

## -see-also

[CreateDirectory2](nf-fileapi-createdirectory2w.md)

[CreateFile3](nf-fileapi-createfile3.md)

[RemoveDirectory2](nf-fileapi-removedirectory2w.md)
