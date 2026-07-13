---
UID: NF:shlwapi.UrlGetPartA
title: UrlGetPartA function (shlwapi.h)
description: Accepts a URL string and returns a specified part of that URL. (ANSI)
helpviewer_keywords: ["URL_PARTFLAG_KEEPSCHEME", "URL_PART_HOSTNAME", "URL_PART_PASSWORD", "URL_PART_PORT", "URL_PART_QUERY", "URL_PART_SCHEME", "URL_PART_USERNAME", "UrlGetPartA", "shlwapi/UrlGetPartA"]
old-location: shell\UrlGetPart.htm
tech.root: shell
ms.assetid: 5f43dedd-c543-46b2-b90e-f0af576d2605
ms.date: 12/05/2018
ms.keywords: URL_PARTFLAG_KEEPSCHEME, URL_PART_HOSTNAME, URL_PART_PASSWORD, URL_PART_PORT, URL_PART_QUERY, URL_PART_SCHEME, URL_PART_USERNAME, UrlGetPart, UrlGetPart function [Windows Shell], UrlGetPartA, UrlGetPartW, _win32_UrlGetPart, shell.UrlGetPart, shlwapi/UrlGetPart, shlwapi/UrlGetPartA, shlwapi/UrlGetPartW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlGetPartW (Unicode) and UrlGetPartA (ANSI)
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
 - UrlGetPartA
 - shlwapi/UrlGetPartA
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
 - UrlGetPart
 - UrlGetPartA
 - UrlGetPartW
---

# UrlGetPartA function


## -description

Accepts a URL string and returns a specified part of that URL.

## -parameters

### -param pszIn [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.

### -param pszOut [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives a null-terminated string with the specified part of the URL.

### -param pcchOut [in, out]

Type: <b>DWORD*</b>

A pointer to a value that, on entry, is set to the number of characters in the <i>pszOut</i> buffer. When this function returns successfully, the value depends on whether the function is successful or returns E_POINTER. For other return values, the value of this parameter is meaningless.

### -param dwPart

Type: <b>DWORD</b>

The flags that specify which part of the URL to retrieve. It can have one of the following values.



#### URL_PART_HOSTNAME

The host name.



#### URL_PART_PASSWORD

The password.



#### URL_PART_PORT

The port number.



#### URL_PART_QUERY

The query portion of the URL.



#### URL_PART_SCHEME

The URL scheme.



#### URL_PART_USERNAME

The username.

### -param dwFlags

Type: <b>DWORD</b>

A flag that can be set to keep the URL scheme, in addition to the part that is specified by <i>dwPart</i>.



#### URL_PARTFLAG_KEEPSCHEME

Keep the URL scheme.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful. The value pointed to by <i>pcchOut</i> will be set to the number of characters written to the output buffer, excluding the terminating <b>NULL</b>. If the buffer was too small, E_POINTER is returned, and the value pointed to by <i>pcchOut</i> will be set to the minimum number of characters that the buffer must be able to contain, including the terminating <b>NULL</b> character. Otherwise, a COM error value is returned.

## -remarks

> [!NOTE]
> The shlwapi.h header defines UrlGetPart as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

