---
UID: NF:shellapi.SHGetDiskFreeSpaceExW
title: SHGetDiskFreeSpaceExW function (shellapi.h)
description: Retrieves disk space information for a disk volume. (Unicode)
helpviewer_keywords: ["SHGetDiskFreeSpace", "SHGetDiskFreeSpaceEx", "SHGetDiskFreeSpaceEx function [Windows Shell]", "SHGetDiskFreeSpaceExW", "_shell_SHGetDiskFreeSpaceEx", "shell.SHGetDiskFreeSpaceEx", "shellapi/SHGetDiskFreeSpaceEx", "shellapi/SHGetDiskFreeSpaceExW"]
old-location: shell\SHGetDiskFreeSpaceEx.htm
tech.root: shell
ms.assetid: f8adbfa8-124a-4934-b5dc-16e261c15a8b
ms.date: 12/05/2018
ms.keywords: SHGetDiskFreeSpace, SHGetDiskFreeSpaceEx, SHGetDiskFreeSpaceEx function [Windows Shell], SHGetDiskFreeSpaceExA, SHGetDiskFreeSpaceExW, _shell_SHGetDiskFreeSpaceEx, shell.SHGetDiskFreeSpaceEx, shellapi/SHGetDiskFreeSpaceEx, shellapi/SHGetDiskFreeSpaceExA, shellapi/SHGetDiskFreeSpaceExW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetDiskFreeSpaceExW (Unicode) and SHGetDiskFreeSpaceExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetDiskFreeSpaceExW
 - shellapi/SHGetDiskFreeSpaceExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetDiskFreeSpaceEx
 - SHGetDiskFreeSpaceExA
 - SHGetDiskFreeSpaceExW
---

# SHGetDiskFreeSpaceExW function


## -description

Retrieves disk space information for a disk volume.

## -parameters

### -param pszDirectoryName [in]

Type: <b>LPCTSTR</b>

A null-terminated string that specifies the volume for which size information is retrieved. This can be a drive letter, UNC name, or the path of a folder. You cannot use <b>NULL</b> to represent the current drive.

### -param pulFreeBytesAvailableToCaller [out, optional]

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a>*</b>

Pointer to a value that receives the number of bytes on the volume available to the calling application. If the operating system implements per-user quotas, this value may be less than the total number of free bytes on the volume.

### -param pulTotalNumberOfBytes [out, optional]

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a>*</b>

Pointer to a value that receives the total size of the volume, in bytes.

### -param pulTotalNumberOfFreeBytes [out, optional]

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a>*</b>

Pointer to a value that receives the number of bytes of free space on the volume.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise.

## -remarks

The similarly named function <a href="/previous-versions/bb762176(v=vs.85)">SHGetDiskFreeSpace</a> is merely an alias for <b>SHGetDiskFreeSpaceEx</b>. When you call <b>SHGetDiskFreeSpace</b> you actually call this function.

This function calls the <a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespaceexa">GetDiskFreeSpaceEx</a> function if it is available on the operating system. If <b>GetDiskFreeSpaceEx</b> is not available, it is emulated by calling the <a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea">GetDiskFreeSpace</a> function and manipulating the return values. For additional information, see the documentation for <b>GetDiskFreeSpaceEx</b>.





> [!NOTE]
> The shellapi.h header defines SHGetDiskFreeSpaceEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespaceexa">GetDiskFreeSpaceEx</a>



<a href="/previous-versions/bb762176(v=vs.85)">SHGetDiskFreeSpace</a>
