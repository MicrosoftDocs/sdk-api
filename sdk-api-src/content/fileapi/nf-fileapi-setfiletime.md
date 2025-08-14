---
UID: NF:fileapi.SetFileTime
title: SetFileTime function (fileapi.h)
description: Sets the date and time that the specified file or directory was created, last accessed, or last modified.
helpviewer_keywords: ["SetFileTime","SetFileTime function","_win32_setfiletime","base.setfiletime","fileapi/SetFileTime","winbase/SetFileTime"]
old-location: base\setfiletime.htm
tech.root: winprog
ms.assetid: 75d988e4-22a3-4084-a5f8-1fca73ccd542
ms.date: 08/30/2022
ms.keywords: SetFileTime, SetFileTime function, _win32_setfiletime, base.setfiletime, fileapi/SetFileTime, winbase/SetFileTime
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - SetFileTime
 - fileapi/SetFileTime
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
 - SetFileTime
---

# SetFileTime function

## -description

Sets the date and time that the specified file or directory was created, last accessed, or last modified.

## -parameters

### -param hFile [in]

A handle to the file or directory. The handle must have been created using the [CreateFile](/windows/win32/api/fileapi/nf-fileapi-createfilea) function  with the **FILE_WRITE_ATTRIBUTES** access right. For more information, see [File Security and Access Rights](/windows/win32/FileIO/file-security-and-access-rights).

### -param lpCreationTime [in, optional]

A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the new creation date and time for the file or directory. If the application does not need to change this information, set this parameter either to `NULL` or to a pointer to a **FILETIME** structure that has both the **dwLowDateTime** and **dwHighDateTime** members set to `0`.

### -param lpLastAccessTime [in, optional]

A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the new last access date and time for the file or directory. The last access time includes the last time the file or directory was written to, read from, or (in the case of executable files) run. If the application does not need to change this information, set this parameter either to `NULL` or to a pointer to a **FILETIME** structure that has both the **dwLowDateTime** and **dwHighDateTime** members set to `0`.

To prevent file operations using the given handle from modifying the last access time, call **SetFileTime** immediately after opening the file handle and pass a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that has both the **dwLowDateTime** and **dwHighDateTime** members set to `0xFFFFFFFF`.

### -param lpLastWriteTime [in, optional]

A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the new last modified date and time for the file or directory.  If the application does not need to change this information, set this parameter either to `NULL` or to a pointer to a **FILETIME** structure that has both the **dwLowDateTime** and **dwHighDateTime** members set to `0`.

To prevent file operations using the given handle from modifying the last write time, call **SetFileTime** immediately after opening the file handle and pass a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that has both the **dwLowDateTime** and **dwHighDateTime** members set to `0xFFFFFFFF`.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

Not all file systems can record creation and last access times and not all file systems record them in the same manner. For example, on  FAT, create time has a resolution of 10 milliseconds, write time has a resolution of 2 seconds, and access time has a resolution of 1 day (really, the access date). Therefore, the [GetFileTime](/windows/win32/api/fileapi/nf-fileapi-getfiletime) function may not return the same file time information set using **SetFileTime**. NTFS delays updates to the last access time for a file by up to one hour after the last access.

### Examples

For an example, see [Changing a File Time to the Current Time](/windows/win32/SysInfo/changing-a-file-time-to-the-current-time).

## -see-also

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

[File Times](/windows/win32/SysInfo/file-times)

[GetFileSize](/windows/win32/api/fileapi/nf-fileapi-getfilesize)

[GetFileTime](/windows/win32/api/fileapi/nf-fileapi-getfiletime)

[GetFileType](/windows/win32/api/fileapi/nf-fileapi-getfiletype)

[SetFileInformationByHandle](/windows/win32/api/fileapi/nf-fileapi-setfileinformationbyhandle)

[Time Functions](/windows/win32/SysInfo/time-functions)
