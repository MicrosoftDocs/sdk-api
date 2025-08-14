---
UID: NF:winbase.GetFileInformationByName
tech.root: fs
title: GetFileInformationByName function (winbase.h)
ms.date: 01/08/2024
targetos: Windows
description: Queries information about a file or directory, given the path to the file.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: winbase.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-file-l2-1-4.dll
 - winbase.h
api_name:
 - GetFileInformationByName
f1_keywords:
 - GetFileInformationByName
 - winbase/GetFileInformationByName
dev_langs:
 - c++
helpviewer_keywords:
 - GetFileInformationByName
---

## -description

Queries information about a file or directory, given the path to the file.

## -parameters

### -param FileName

The file name/path.

### -param FileInformationClass

Specifies the type of information that should be retrieved.

### -param FileInfoBuffer

A pointer to a buffer where the retrieved data will be stored.

### -param FileInfoBufferSize

Specifies the size of the *FileInfoBuffer* buffer.

## -returns

If the function fails, the return value is **FALSE**, otherwise **TRUE**. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

This routine returns the requested information about the file specified by *FileName*. It does so without opening and returning a handle to the file. The information returned is determined by the *FileInformationClass* that is specified and is placed into the caller's buffer.

The *FileInformationClass* argument must be one of the following values from the [FILE_INFO_BY_NAME_CLASS](../minwinbase/ne-minwinbase-file_info_by_name_class.md) enumeration. The following list describes the type which must be used for the *FileInfoBuffer* parameter:

| FileInformationClass type | FileInfoBuffer type |
|---------------------------|---------------------|
| **FileStatByNameInfo** | The file info buffer should be an instance of [FILE_STAT_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_information). |
| **FileStatLxByNameInfo** | The file info buffer should be an instance of [FILE_STAT_LX_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_lx_information). |
| **FileCaseSensitiveByNameInfo** | The file info buffer should be an instance of [FILE_CASE_SENSITIVE_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_case_sensitive_information). |
| **FileStatBasicByNameInfo** | The file info buffer should be an instance of [FILE_STAT_BASIC_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-file_stat_basic_information). |

#### Examples

The following shows an example of querying information of file information class **FileStatByNameInfo** by filepath using **GetFileInformationByName**. See [FILE_STAT_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_information) for additional details on the query results.

```cpp
#include <windows.h> 
#include <winnt.h> 
#include <stdio.h> 

DWORD
GetFileStatInfoByName(
    _In_ PCWSTR FilePath)
{
    DWORD Status = ERROR_SUCCESS;
    FILE_STAT_INFORMATION FileStatInfo;

    if (!GetFileInformationByName(FilePath,
                                  FileStatByNameInfo,
                                  &FileStatInfo,
                                  sizeof(FileStatInfo)))
    {
        Status = GetLastError();
        fwprintf_s(stderr, L"GetFileInformationByName() failed; error %u\n", Status);
    }
    else
    {
        fwprintf_s(stdout, L"FileId             0x%I64X\n",     FileStatInfo.FileId.QuadPart);
        fwprintf_s(stdout, L"CreationTime       0x%I64X\n",     FileStatInfo.CreationTime.QuadPart);
        fwprintf_s(stdout, L"LastAccessTime     0x%I64X\n",     FileStatInfo.LastAccessTime.QuadPart);
        fwprintf_s(stdout, L"LastWriteTime      0x%I64X\n",     FileStatInfo.LastWriteTime.QuadPart);
        fwprintf_s(stdout, L"ChangeTime         0x%I64X\n",     FileStatInfo.ChangeTime.QuadPart);
        fwprintf_s(stdout, L"AllocationSize     0x%I64X\n",     FileStatInfo.AllocationSize.QuadPart);
        fwprintf_s(stdout, L"EndOfFile          0x%I64X\n",     FileStatInfo.EndOfFile.QuadPart);
        fwprintf_s(stdout, L"FileAttributes     0x%08X\n",      FileStatInfo.FileAttributes);
        fwprintf_s(stdout, L"ReparseTag         0x%08X\n",      FileStatInfo.ReparseTag);
        fwprintf_s(stdout, L"NumberOfLinks      %u\n",          FileStatInfo.NumberOfLinks);
        fwprintf_s(stdout, L"EffectiveAccess    0x%08X\n",      FileStatInfo.EffectiveAccess);
    }

    return Status;
} 
```

The following shows an example of querying information of file information class **FileStatLxByNameInfo** by filepath using **GetFileInformationByName**. See [FILE_STAT_LX_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_lx_information) for additional details on the query results.

```cpp
#include <windows.h> 
#include <winnt.h> 
#include <stdio.h> 

DWORD
GetFileStatLxInfoByName(
    _In_ PCWSTR FilePath)
{
    FILE_STAT_LX_INFORMATION FileStatInfo;
    DWORD Status = ERROR_SUCCESS;

    if (!GetFileInformationByName(FilePath,
                                  FileStatLxByNameInfo,
                                  &FileStatInfo,
                                  sizeof(FileStatInfo)))
    {
        Status = GetLastError();
        fwprintf_s(stderr, L"GetFileInformationByName() failed; error %u\n", Status);
    }
    else
    {
        fwprintf_s(stdout, L"FileId             0x%I64X\n",     FileStatInfo.FileId.QuadPart);
        fwprintf_s(stdout, L"CreationTime       0x%I64X\n",     FileStatInfo.CreationTime.QuadPart);
        fwprintf_s(stdout, L"LastAccessTime     0x%I64X\n",     FileStatInfo.LastAccessTime.QuadPart);
        fwprintf_s(stdout, L"LastWriteTime      0x%I64X\n",     FileStatInfo.LastWriteTime.QuadPart);
        fwprintf_s(stdout, L"ChangeTime         0x%I64X\n",     FileStatInfo.ChangeTime.QuadPart);
        fwprintf_s(stdout, L"AllocationSize     0x%I64X\n",     FileStatInfo.AllocationSize.QuadPart);
        fwprintf_s(stdout, L"EndOfFile          0x%I64X\n",     FileStatInfo.EndOfFile.QuadPart);
        fwprintf_s(stdout, L"FileAttributes     0x%08X\n",      FileStatInfo.FileAttributes);
        fwprintf_s(stdout, L"ReparseTag         0x%08X\n",      FileStatInfo.ReparseTag);
        fwprintf_s(stdout, L"NumberOfLinks      %u\n",          FileStatInfo.NumberOfLinks);
        fwprintf_s(stdout, L"LxFlags            0x%08X\n",      FileStatInfo.LxFlags);
        fwprintf_s(stdout, L"LxUid              0x%08X\n",      FileStatInfo.LxUid);
        fwprintf_s(stdout, L"LxGid              0x%08X\n",      FileStatInfo.LxGid);
        fwprintf_s(stdout, L"LxMode             0x%08X\n",      FileStatInfo.LxMode);
        fwprintf_s(stdout, L"LxDeviceIdMajor    0x%08X\n",      FileStatInfo.LxDeviceIdMajor);
        fwprintf_s(stdout, L"LxDeviceIdMinor    0x%08X\n",      FileStatInfo.LxDeviceIdMinor);
    }

    return Status;
}
```

The following shows an example of querying case-sensitive information for file information class **FileCaseSensitiveByNameInfo** with a filepath by using **GetFileInformationByName**. See [FILE_CASE_SENSITIVE_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_case_sensitive_information) for additional details on the query results.

```cpp
#include <windows.h>
#include <winnt.h>
#include <stdio.h>

DWORD
GetFileStatCaseSensitiveInfoByName(
    _In_ PCWSTR FilePath)
{
    DWORD Status = ERROR_SUCCESS;
    FILE_CASE_SENSITIVE_INFORMATION FileStatInfo;

    if (!GetFileInformationByName(FilePath,
                                  FileCaseSensitiveByNameInfo,
                                  &FileStatInfo,
                                  sizeof(FileStatInfo)))
    {
        Status = GetLastError();
        fwprintf_s(stderr, L"GetFileStatCaseSensitiveInfoByName() failed; error %u\n", Status);
    }
    else
    {
        fwprintf_s(stdout, L"Flags              0x%08X\n",      FileStatInfo.Flags);

    }

    return Status;
}
```

The following shows an example of querying information of file information class **FileStatBasicByNameInfo** with a filepath by using **GetFileInformationByName**. See **FILE_STAT_BASIC_INFORMATION** for additional details on the query results.

```cpp
#include <windows.h>
#include <winnt.h>
#include <stdio.h>

DWORD
GetFileStatBasicInfoByName(
    _In_ PCWSTR FilePath)
{
    DWORD Status = ERROR_SUCCESS;
    FILE_STAT_BASIC_INFORMATION FileStatInfo;

    if (!GetFileInformationByName(FilePath,
                                  FileStatBasicByNameInfo,
                                  &FileStatInfo,
                                  sizeof(FileStatInfo)))
    {
        Status = GetLastError();
        fwprintf_s(stderr, L"GetFileInformationByName failed; error %u\n", Status);
    }
    else
    {
        fwprintf_s(stdout, L"FileId             0x%I64X\n",     FileStatInfo.FileId.QuadPart);
        fwprintf_s(stdout, L"CreationTime       0x%I64X\n",     FileStatInfo.CreationTime.QuadPart);
        fwprintf_s(stdout, L"LastAccessTime     0x%I64X\n",     FileStatInfo.LastAccessTime.QuadPart);
        fwprintf_s(stdout, L"LastWriteTime      0x%I64X\n",     FileStatInfo.LastWriteTime.QuadPart);
        fwprintf_s(stdout, L"ChangeTime         0x%I64X\n",     FileStatInfo.ChangeTime.QuadPart);
        fwprintf_s(stdout, L"AllocationSize     0x%I64X\n",     FileStatInfo.AllocationSize.QuadPart);
        fwprintf_s(stdout, L"EndOfFile          0x%I64X\n",     FileStatInfo.EndOfFile.QuadPart);
        fwprintf_s(stdout, L"FileAttributes     0x%08X\n",      FileStatInfo.FileAttributes);
        fwprintf_s(stdout, L"ReparseTag         0x%08X\n",      FileStatInfo.ReparseTag);
        fwprintf_s(stdout, L"NumberOfLinks      %u\n",          FileStatInfo.NumberOfLinks);
    }

    return Status;
}
```

## -see-also

- [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
- [FILE_INFO_BY_NAME_CLASS](../minwinbase/ne-minwinbase-file_info_by_name_class.md)
- [FILE_STAT_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_information)
- [FILE_STAT_LX_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_lx_information)
- [FILE_CASE_SENSITIVE_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_case_sensitive_information)
- [FILE_STAT_BASIC_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-file_stat_basic_information)
