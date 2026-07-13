---
UID: NF:shlwapi.UrlUnescapeW
title: UrlUnescapeW function (shlwapi.h)
description: Converts escape sequences back into ordinary characters. (Unicode)
helpviewer_keywords: ["URL_DONT_UNESCAPE_EXTRA_INFO", "URL_UNESCAPE_AS_UTF8", "URL_UNESCAPE_INPLACE", "UrlUnescape", "UrlUnescape function [Windows Shell]", "UrlUnescapeW", "_win32_UrlUnescape", "shell.UrlUnescape", "shlwapi/UrlUnescape", "shlwapi/UrlUnescapeW"]
old-location: shell\UrlUnescape.htm
tech.root: shell
ms.assetid: 5bff5161-3b57-4f12-b126-42eac3f60267
ms.date: 12/05/2018
ms.keywords: URL_DONT_UNESCAPE_EXTRA_INFO, URL_UNESCAPE_AS_UTF8, URL_UNESCAPE_INPLACE, UrlUnescape, UrlUnescape function [Windows Shell], UrlUnescapeA, UrlUnescapeW, _win32_UrlUnescape, shell.UrlUnescape, shlwapi/UrlUnescape, shlwapi/UrlUnescapeA, shlwapi/UrlUnescapeW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlUnescapeW (Unicode) and UrlUnescapeA (ANSI)
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
 - UrlUnescapeW
 - shlwapi/UrlUnescapeW
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
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - UrlUnescape
 - UrlUnescapeA
 - UrlUnescapeW
---

# UrlUnescapeW function


## -description

Converts escape sequences back into ordinary characters.

## -parameters

### -param pszUrl [in, out]

Type: <b>PTSTR</b>

A pointer to a null-terminated string with the URL. If <i>dwFlags</i> is set to <b>URL_UNESCAPE_INPLACE</b>, the converted string is returned through this parameter.

### -param pszUnescaped [out, optional]

Type: <b>PTSTR</b>

A pointer to a buffer that will receive a null-terminated string that contains the unescaped version of <i>pszURL</i>. If <b>URL_UNESCAPE_INPLACE</b> is set in <i>dwFlags</i>, this parameter is ignored.

### -param pcchUnescaped [in, out, optional]

Type: <b>DWORD*</b>

The number of characters in the buffer pointed to by <i>pszUnescaped</i>. On entry, the value <i>pcchUnescaped</i> points to is set to the size of the buffer. If the function returns a success code and the <b>URL_UNESCAPE_INPLACE</b> flag is not set, the value that <i>pcchUnescaped</i> points to is set to the number of characters written to that buffer, not counting the terminating <b>NULL</b> character. If an E_POINTER error code is returned, the buffer was too small, and the value to which <i>pcchUnescaped</i> points is set to the required number of characters that the buffer must be able to contain. If any other errors are returned, the value to which <i>pcchUnescaped</i> points is undefined.

### -param dwFlags

Type: <b>DWORD</b>

Flags that control which characters are unescaped. It can be a combination of the following flags.



#### URL_DONT_UNESCAPE_EXTRA_INFO

Do not convert the # or ? character, or any characters following them in the string.



#### URL_UNESCAPE_AS_UTF8

<b>Introduced in Windows 8</b>. Decode URLs that were encoded by using the <b>URL_ESCAPE_AS_UTF8</b> flag.



#### URL_UNESCAPE_INPLACE

Use <i>pszURL</i> to return the converted string instead of <i>pszUnescaped</i>.


##### - dwFlags.URL_DONT_UNESCAPE_EXTRA_INFO

Do not convert the # or ? character, or any characters following them in the string.


##### - dwFlags.URL_UNESCAPE_AS_UTF8

<b>Introduced in Windows 8</b>. Decode URLs that were encoded by using the <b>URL_ESCAPE_AS_UTF8</b> flag.


##### - dwFlags.URL_UNESCAPE_INPLACE

Use <i>pszURL</i> to return the converted string instead of <i>pszUnescaped</i>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful. If the <b>URL_UNESCAPE_INPLACE</b> flag is not set, the value pointed to by <i>pcchUnescaped</i> will be set to the number of characters in the output buffer pointed to by <i>pszUnescaped</i>. Returns E_POINTER if the <b>URL_UNESCAPE_INPLACE</b> flag is not set and the output buffer is too small. The <i>pcchUnescaped</i> parameter will be set to the required buffer size. Otherwise, returns a standard error value.

## -remarks

An escape sequence has the form "%xy".

Input strings cannot be longer than INTERNET_MAX_URL_LENGTH.




> [!NOTE]
> The shlwapi.h header defines UrlUnescape as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

