---
UID: NF:fileapi.RemoveDirectoryA
title: RemoveDirectoryA function (fileapi.h)
description: Deletes an existing empty directory. (ANSI)
helpviewer_keywords: ["RemoveDirectoryA", "fileapi/RemoveDirectoryA"]
old-location: fs\removedirectory.htm
tech.root: fs
ms.assetid: d699cdd2-e270-4f17-bdec-6eea25b01578
ms.date: 12/15/2023
ms.keywords: RemoveDirectory, RemoveDirectory function [Files], RemoveDirectoryA, RemoveDirectoryW, _win32_removedirectory, base.removedirectory, fileapi/RemoveDirectory, fileapi/RemoveDirectoryA, fileapi/RemoveDirectoryW, fs.removedirectory, winbase/RemoveDirectory, winbase/RemoveDirectoryA, winbase/RemoveDirectoryW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveDirectoryW (Unicode) and RemoveDirectoryA (ANSI)
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
 - RemoveDirectoryA
 - fileapi/RemoveDirectoryA
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
 - RemoveDirectory
 - RemoveDirectoryA
 - RemoveDirectoryW
---

# RemoveDirectoryA function

## -description

Deletes an existing empty directory.

To perform this operation as a transacted operation, use the [RemoveDirectoryTransacted](/windows/win32/api/winbase/nf-winbase-removedirectorytransacteda) function.

## -parameters

### -param lpPathName [in]

The path of the directory to be removed. This path must specify an empty directory, and the calling process must have delete access to the directory.

By default, the name is limited to **MAX_PATH** characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the **MAX_PATH** limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The **RemoveDirectory** function marks a directory for deletion on close. Therefore, the directory is not removed until the last handle to the directory is closed.

To recursively delete the files in a directory, use the [SHFileOperation](/windows/win32/api/shellapi/nf-shellapi-shfileoperationa) function.

**RemoveDirectory** can be used to remove a directory junction. Since the target directory and its contents will remain accessible through its canonical path, the target directory itself is not affected by removing a junction which targets it. For this reason, when *lpPathName* refers to a directory junction, **RemoveDirectory** will remove the specified link regardless of whether the target directory is empty or not. For more information on junctions, see [Hard Links and Junctions](/windows/win32/FileIO/hard-links-and-junctions).

The use of POSIX delete causes the directory to be deleted while handles remain open. Subsequent calls to [CreateDirectory](nf-fileapi-createdirectorya.md) to open the directory fail with **ERROR_FILE_NOT_FOUND**.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies:

| Technology | Supported |
| --- | --- |
| Server Message Block (SMB) 3.0 protocol | Yes |
| SMB 3.0 Transparent Failover (TFO) | Yes |
| SMB 3.0 with Scale-out File Shares (SO) | Yes |
| Cluster Shared Volume File System (CsvFS) | Yes |
| Resilient File System (ReFS) | Yes |

> [!NOTE]
> The fileapi.h header defines RemoveDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[CreateDirectory](/windows/win32/api/fileapi/nf-fileapi-createdirectorya)

[Creating and Deleting Directories](/windows/win32/FileIO/creating-and-deleting-directories)

[Directory Management Functions](/windows/win32/FileIO/directory-management-functions)

[RemoveDirectoryTransacted](/windows/win32/api/winbase/nf-winbase-removedirectorytransacteda)
