---
UID: NF:winbase.GetDllDirectoryA
title: GetDllDirectoryA function (winbase.h)
description: Retrieves the application-specific portion of the search path used to locate DLLs for the application. (ANSI)
helpviewer_keywords: ["GetDllDirectoryA", "winbase/GetDllDirectoryA"]
old-location: base\getdlldirectory.htm
tech.root: base
ms.assetid: f892546a-6c48-48f2-8d9a-46e448fffb89
ms.date: 12/05/2018
ms.keywords: GetDllDirectory, GetDllDirectory function, GetDllDirectoryA, GetDllDirectoryW, base.getdlldirectory, winbase/GetDllDirectory, winbase/GetDllDirectoryA, winbase/GetDllDirectoryW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDllDirectoryW (Unicode) and GetDllDirectoryA (ANSI)
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
 - GetDllDirectoryA
 - winbase/GetDllDirectoryA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - Kernel32Legacy.dll
api_name:
 - GetDllDirectory
 - GetDllDirectoryA
 - GetDllDirectoryW
---

# GetDllDirectoryA function


## -description

Retrieves the application-specific portion of the search path used to locate DLLs for the 
   application.

## -parameters

### -param nBufferLength [in]

The size of the output buffer, in characters.

### -param lpBuffer [out]

A pointer to a buffer that receives the application-specific portion of the search path.

## -returns

If the function succeeds, the return value is the length of the string copied to 
       <i>lpBuffer</i>, in characters, not including the terminating null character. If the return 
       value is greater than <i>nBufferLength</i>, it specifies the size of the buffer required for 
       the path.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0502 
    or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.





> [!NOTE]
> The winbase.h header defines GetDllDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Dlls/dynamic-link-library-search-order">Dynamic-Link Library Search Order</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setdlldirectorya">SetDllDirectory</a>
