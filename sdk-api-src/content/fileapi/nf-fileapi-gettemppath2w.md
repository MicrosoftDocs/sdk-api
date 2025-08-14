---
UID: NF:fileapi.GetTempPath2W
title: GetTempPath2W
ms.date: 03/11/2025
ms.topic: language-reference
targetos: Windows
description: Retrieves the path of the directory designated for temporary files, based on the privileges of the calling process. (Unicode)
helpviewer_keywords: ["GetTempPath2", "GetTempPath2 function [Files]", "GetTempPath2W", "GetTempPath2W", "fileapi/GetTempPath2W", "fileapi/GetTempPath2"]
tech.root: fs
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
req.target-min-winverclnt: Windows 11 Build 22000
req.target-min-winversvr: Windows Server 2022 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: GetTempPath2W (Unicode) and GetTempPath2A (ANSI) 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-3.dll
 - api-ms-win-core-file-l1-2-4.dll
 - kernel32.dll
 - kernelbase.dll
api_name:
 - GetTempPath2W
f1_keywords:
 - GetTempPath2W
 - fileapi/GetTempPath2W
dev_langs:
 - c++
---

## -description

Retrieves the path of the directory designated for temporary files, based on the privileges of the calling process.

## -parameters

### -param BufferLength [in]

The size of the string buffer identified by *lpBuffer*, in **TCHARs**.

### -param Buffer [out]

A pointer to a string buffer that receives the null-terminated string specifying the temporary file path. The returned string ends with a backslash, for example, "C:\\TEMP\\".

## -returns

If the function succeeds, the return value is the length, in **TCHARs**, of the string copied to *lpBuffer*, not including the terminating null character. If the return value is greater than *nBufferLength*, the return value is the length, in **TCHARs**, of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

The maximum possible return value is **MAX_PATH**+1 (261).

## -remarks

When calling this function from a process running as SYSTEM it will return the path C:\Windows\SystemTemp, which is inaccessible to non-SYSTEM processes. For non-SYSTEM processes, **GetTempPath2** will behave the same as [GetTempPath](/windows/win32/api/fileapi/nf-fileapi-gettemppatha).

For system processes, the **GetTempPath2** function checks for the existence of the environment variable `SystemTemp`. If this environment variable is set, it will use the value of the environment variable as the path instead of the default system provided path on the `C:` drive.

> [!NOTE]
> The reason **GetTempPath2** exists and defaults to returning C:\Windows\SystemTemp is because that directory is ACL'd with the correct permissions to prevent common path redirection issues. For security reasons, only set the SystemTemp environment variable to a directory with permissions that only allow for a SYSTEM process/administrator to access it.

For non-system processes, the **GetTempPath2** function checks for the existence of environment variables in the following order and uses the first path found:

1. The path specified by the TMP environment variable.
1. The path specified by the TEMP environment variable.
1. The path specified by the USERPROFILE environment variable.
1. The Windows directory.

Note that the function does not verify that the path exists, nor does it test to see if the current process has any kind of access rights to the path. The **GetTempPath2** function returns the properly formatted string that specifies the fully qualified path based on the environment variable search order as previously specified. The application should verify the existence of the path and adequate access rights to the path prior to any use for file I/O operations.

**Symbolic link behavior:** If the path points to a symbolic link, the temp path name maintains any symbolic links.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

| Technology | Supported |
| --- | --- |
| Server Message Block (SMB) 3.0 protocol | Yes |
| SMB 3.0 Transparent Failover (TFO) | Yes |
| SMB 3.0 with Scale-out File Shares (SO) | Yes |
| Cluster Shared Volume File System (CsvFS) | Yes |
| Resilient File System (ReFS) | Yes |

> [!NOTE]
> When Windows updates released in March 2025 and later are installed, this API will be supported on Windows 10, version 1607 (Build 14393.7876) and later and Windows Server 2016 Build 14393.7876 and later versions. See [KB5053594](https://support.microsoft.com/topic/march-11-2025-kb5053594-os-build-14393-7876-831b6318-8f05-4c41-b413-509fb89baa34) for more information.

#### Examples

For an example, see [Creating and Using a Temporary File](/windows/win32/FileIO/creating-and-using-a-temporary-file).

> [!NOTE]
> The `fileapi.h` header defines **GetTempPath2** as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[File Management Functions](/windows/win32/FileIO/file-management-functions)

[GetTempFileName](nf-fileapi-gettempfilenamew.md)

[Symbolic Links](/windows/win32/FileIO/symbolic-links)
