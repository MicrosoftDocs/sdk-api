---
UID: NF:fileapi.RemoveDirectory2A
tech.root: fs
title: RemoveDirectory2A function (fileapi.h)
ms.date: 04/10/2025
targetos: Windows
description: Deletes an existing empty directory. (ANSI)
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
 - RemoveDirectory2A
 - RemoveDirectory2
f1_keywords:
 - RemoveDirectory2A
 - fileapi/RemoveDirectory2A
 - RemoveDirectory2
 - fileapi/RemoveDirectory2
dev_langs:
 - c++
helpviewer_keywords:
 - RemoveDirectory2A
---

## -description

Deletes an existing empty directory. This function will fail if any part of *lpPathName* is redirected via a reparse point or symbolic link.

To perform this operation as a transacted operation, use the [RemoveDirectoryTransacted](../winbase/nf-winbase-removedirectorytransacteda.md) function.

## -parameters

### -param lpPathName

The path of the directory to be removed. This path must specify an empty directory, and the calling process must have delete access to the directory.

By default, the name is limited to **MAX_PATH** characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> You can opt-in to remove the **MAX_PATH** limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param DirectoryFlags

Flags that specify how the directory is to be deleted. This parameter can be a combination of the following values:

| Value | Meaning |
|-------|---------|
| **DIRECTORY_FLAGS_DISALLOW_PATH_REDIRECTS**<br/>`0x00000001` | Prevent *lpPathName* from being redirected by reparse points or symbolic links. |

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

The **RemoveDirectory2** function marks a directory for deletion on close. Therefore, the directory is not removed until the last handle to the directory is closed.

To recursively delete the files in a directory, use the [SHFileOperation](../shellapi/nf-shellapi-shfileoperationa.md) function.

**RemoveDirectory2** can be used to remove a directory junction. Since the target directory and its contents will remain accessible through its canonical path, the target directory itself is not affected by removing a junction which targets it. For this reason, when *lpPathName* refers to a directory junction, **RemoveDirectory2** will remove the specified link regardless of whether the target directory is empty or not. For more information on junctions, see [Hard Links and Junctions](/windows/win32/fileio/hard-links-and-junctions).

The use of POSIX delete causes the directory to be deleted while handles remain open. Subsequent calls to [CreateDirectory](nf-fileapi-createdirectorya.md) or [CreateDirectory2](nf-fileapi-createdirectory2a.md) to open the directory fail with **ERROR_FILE_NOT_FOUND**.

This function is supported by the following technologies:

| Technology | Supported |
| --- | --- |
| Server Message Block (SMB) 3.0 protocol | Yes |
| SMB 3.0 Transparent Failover (TFO) | Yes |
| SMB 3.0 with Scale-out File Shares (SO) | Yes |
| Cluster Shared Volume File System (CsvFS) | Yes |
| Resilient File System (ReFS) | Yes |

> [!NOTE]
> The `fileapi.h` header defines **RemoveDirectory2** as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[CreateDirectory2](nf-fileapi-createdirectory2a.md)

[Creating and Deleting Directories](/windows/win32/fileio/creating-and-deleting-directories)

[Directory Management Functions](/windows/win32/fileio/directory-management-functions)

[RemoveDirectoryTransacted](../winbase/nf-winbase-removedirectorytransacteda.md)
