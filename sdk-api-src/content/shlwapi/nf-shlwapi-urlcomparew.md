---
UID: NF:shlwapi.UrlCompareW
title: UrlCompareW function (shlwapi.h)
description: Makes a case-sensitive comparison of two URL strings. (Unicode)
helpviewer_keywords: ["UrlCompare", "UrlCompare function [Windows Shell]", "UrlCompareW", "_win32_UrlCompare", "shell.UrlCompare", "shlwapi/UrlCompare", "shlwapi/UrlCompareW"]
old-location: shell\UrlCompare.htm
tech.root: shell
ms.assetid: d5c9e003-b85b-4f9f-b231-e3e4b71d4ce6
ms.date: 12/05/2018
ms.keywords: UrlCompare, UrlCompare function [Windows Shell], UrlCompareA, UrlCompareW, _win32_UrlCompare, shell.UrlCompare, shlwapi/UrlCompare, shlwapi/UrlCompareA, shlwapi/UrlCompareW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlCompareW (Unicode) and UrlCompareA (ANSI)
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
 - UrlCompareW
 - shlwapi/UrlCompareW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-url-l1-1-0.dll
 - KernelBase.dll
api_name:
 - UrlCompare
 - UrlCompareA
 - UrlCompareW
---

# UrlCompareW function


## -description

Makes a case-sensitive comparison of two URL strings.

## -parameters

### -param psz1 [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the first URL.

### -param psz2 [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the second URL.

### -param fIgnoreSlash

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> to have <b>UrlCompare</b> ignore a trailing '/' character on either or both URLs.

## -returns

Type: <b>int</b>

Returns zero if the two strings are equal. The function will also return zero if <i>fIgnoreSlash</i> is set to <b>TRUE</b> and one of the strings has a trailing '\' character. The function returns a negative integer if the string pointed to by <i>psz1</i> is less than the string pointed to by <i>psz2</i>. Otherwise, it returns a positive integer.

## -remarks

For best results, you should first canonicalize the URLs with <a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlcanonicalizea">UrlCanonicalize</a>. Then, compare the canonicalized URLs with <b>UrlCompare</b>.





> [!NOTE]
> The shlwapi.h header defines UrlCompare as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strcmpw">StrCmp</a>
