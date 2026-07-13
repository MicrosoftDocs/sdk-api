---
UID: NF:shlwapi.SHStrDupA
title: SHStrDupA function (shlwapi.h)
description: Makes a copy of a string in newly allocated memory. (SHStrDupA)
helpviewer_keywords: ["SHStrDupA", "shlwapi/SHStrDupA"]
old-location: shell\SHStrDup.htm
tech.root: shell
ms.assetid: 6f014fb4-7637-48a8-9bec-d3278c46a6d8
ms.date: 12/05/2018
ms.keywords: SHStrDup, SHStrDup function [Windows Shell], SHStrDupA, SHStrDupW, _win32_SHStrDup, shell.SHStrDup, shlwapi/SHStrDup, shlwapi/SHStrDupA, shlwapi/SHStrDupW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHStrDupW (Unicode) and SHStrDupA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHStrDupA
 - shlwapi/SHStrDupA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-Obsolete-l1-1-0.dll
api_name:
 - SHStrDup
 - SHStrDupA
 - SHStrDupW
---

# SHStrDupA function


## -description

Makes a copy of a string in newly allocated memory.

## -parameters

### -param psz [in]

Type: <b>LPCTSTR</b>

A pointer to the null-terminated string to be copied.

### -param ppwsz [out]

Type: <b>LPTSTR*</b>

A pointer to an allocated Unicode string that contains the result. <b>SHStrDup</b> allocates memory for this string with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. You should free the string with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when it is no longer needed.

                    

In the case of failure, this value is NULL.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.

## -remarks

This function will take either Unicode or ANSI strings as input, but the copied string is always Unicode.

This function uses <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> to allocate memory for the copied string. You must free this memory with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when it is no longer needed.





> [!NOTE]
> The shlwapi.h header defines SHStrDup as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strdupa">StrDup</a>
