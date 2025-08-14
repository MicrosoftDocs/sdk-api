---
UID: NF:wow64apiset.GetSystemWow64DirectoryW
title: GetSystemWow64DirectoryW function (wow64apiset.h)
description: Retrieves the path of the system directory used by WOW64. (Unicode)
helpviewer_keywords: ["GetSystemWow64Directory", "GetSystemWow64Directory function", "GetSystemWow64DirectoryW", "_win32_getsystemwow64directory", "base.getsystemwow64directory", "wow64apiset/GetSystemWow64Directory", "wow64apiset/GetSystemWow64DirectoryW"]
old-location: base\getsystemwow64directory.htm
tech.root: fs
ms.assetid: 31ccd1bf-87c7-4df6-ae9d-5a3dfbd8b38b
ms.date: 12/05/2018
ms.keywords: GetSystemWow64Directory, GetSystemWow64Directory function, GetSystemWow64DirectoryA, GetSystemWow64DirectoryW, _win32_getsystemwow64directory, base.getsystemwow64directory, wow64apiset/GetSystemWow64Directory, wow64apiset/GetSystemWow64DirectoryA, wow64apiset/GetSystemWow64DirectoryW
req.header: wow64apiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSystemWow64DirectoryW (Unicode) and GetSystemWow64DirectoryA (ANSI)
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
 - GetSystemWow64DirectoryW
 - wow64apiset/GetSystemWow64DirectoryW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-wow64-l1-1-3.dll
 - api-ms-win-core-wow64-l1-1-2.dll
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Wow64-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetSystemWow64Directory
 - GetSystemWow64DirectoryA
 - GetSystemWow64DirectoryW
---

# GetSystemWow64DirectoryW function


## -description

Retrieves the path of the system directory used by WOW64. This directory is not present on 32-bit Windows.

## -parameters

### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash.

### -param uSize [in]

The maximum size of the buffer, in <b>TCHARs</b>.

## -returns

If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the string copied to the buffer, not including the terminating null character. If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

On 32-bit Windows, the function always fails, and the extended error is set to ERROR_CALL_NOT_IMPLEMENTED.

## -remarks

WOW64 uses the system directory to store shared 32-bit code on 64-bit Windows. Most applications have no need to access this directory explicitly.

For more information on WOW64, see 
<a href="/windows/desktop/WinProg64/running-32-bit-applications">Running 32-bit Applications</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.





> [!NOTE]
> The wow64apiset.h header defines GetSystemWow64Directory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SysInfo/system-information-functions">System
    Information Functions</a>
