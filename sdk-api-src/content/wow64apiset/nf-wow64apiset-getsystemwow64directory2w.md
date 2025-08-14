---
UID: NF:wow64apiset.GetSystemWow64Directory2W
title: GetSystemWow64Directory2W function (wow64apiset.h)
description: Retrieves the path of the system directory used by WOW64, using the specified image file machine type. (Unicode)
helpviewer_keywords: ["GetSystemWow64Directory2", "GetSystemWow64Directory2 function", "GetSystemWow64Directory2W", "base.getsystemwow64directory2", "wow64apiset/GetSystemWow64Directory2", "wow64apiset/GetSystemWow64Directory2W"]
old-location: base\getsystemwow64directory2.htm
tech.root: fs
ms.assetid: 938370BE-6EAB-4198-9AF3-ED8889E1E41F
ms.date: 12/05/2018
ms.keywords: GetSystemWow64Directory2, GetSystemWow64Directory2 function, GetSystemWow64Directory2A, GetSystemWow64Directory2W, base.getsystemwow64directory2, wow64apiset/GetSystemWow64Directory2, wow64apiset/GetSystemWow64Directory2A, wow64apiset/GetSystemWow64Directory2W
req.header: wow64apiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1511 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSystemWow64Directory2W (Unicode) and GetSystemWow64Directory2A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.dll
req.dll: Kernel32.lib
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSystemWow64Directory2W
 - wow64apiset/GetSystemWow64Directory2W
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
 - kernel32.lib
 - API-MS-Win-Core-Wow64-L1-1-1.dll
 - KernelBase.dll
api_name:
 - GetSystemWow64Directory2
 - GetSystemWow64Directory2A
 - GetSystemWow64Directory2W
---

# GetSystemWow64Directory2W function


## -description

Retrieves the path of the system directory used by <a href="/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a>, using the specified image file machine type. This directory is not present on 32-bit Windows.

## -parameters

### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash.

### -param uSize [in]

The maximum size of the buffer, in <b>TCHARs</b>.

### -param ImageFileMachineType [in]

An <a href="/windows/desktop/SysInfo/image-file-machine-constants">IMAGE_FILE_MACHINE_*</a> value that specifies the machine to test.

## -returns

If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the string copied to the buffer, not including the terminating null character. If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

On systems that support multiple <a href="/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a> architectures, you can use <b>GetSystemWow64Directory2</b> to retrieve appropriate system directory associated with the WOW64 architecture specified by <i>ImageFileMachineType</i>. 

WOW64 uses the system directory to store shared 32-bit code on 64-bit Windows. Most applications have no need to access this directory explicitly.

For more information on WOW64, see 
<a href="/windows/desktop/WinProg64/running-32-bit-applications">Running 32-bit Applications</a>.





> [!NOTE]
> The wow64apiset.h header defines GetSystemWow64Directory2 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya">GetSystemWow64Directory</a>
