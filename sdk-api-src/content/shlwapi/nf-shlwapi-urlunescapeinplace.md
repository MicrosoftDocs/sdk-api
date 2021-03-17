---
UID: NF:shlwapi.UrlUnescapeInPlace
title: UrlUnescapeInPlace macro (shlwapi.h)
description: Converts escape sequences back into ordinary characters and overwrites the original string.
helpviewer_keywords: ["URL_DONT_UNESCAPE_EXTRA_INFO","UrlUnescapeInPlace","UrlUnescapeInPlace function [Windows Shell]","_win32_UrlUnescapeInPlace","shell.UrlUnescapeInPlace","shlwapi/UrlUnescapeInPlace"]
old-location: shell\UrlUnescapeInPlace.htm
tech.root: shell
ms.assetid: 315215dc-c074-4abb-8bb2-006eff18b88d
ms.date: 12/05/2018
ms.keywords: URL_DONT_UNESCAPE_EXTRA_INFO, UrlUnescapeInPlace, UrlUnescapeInPlace function [Windows Shell], _win32_UrlUnescapeInPlace, shell.UrlUnescapeInPlace, shlwapi/UrlUnescapeInPlace
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - UrlUnescapeInPlace
 - shlwapi/UrlUnescapeInPlace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - UrlUnescapeInPlace
---

# UrlUnescapeInPlace macro


## -description

Converts escape sequences back into ordinary characters and overwrites the original string.

## -parameters

### -param pszUrl [in, out]

Type: <b>LPTSTR</b>

A pointer to a <b>null</b>-terminated string that contains the URL. The converted string is returned through this parameter.

### -param dwFlags [in]

Type: <b>DWORD</b>

The flags that control which characters are unescaped.



#### URL_DONT_UNESCAPE_EXTRA_INFO

Do not convert the # or ? character, or any characters following them in the string.

## -remarks

<b>UrlUnescapeInPlace</b> is equivalent to the following:
				


```

UrlUnescape(pszUrl, NULL, NULL, dwFlags | URL_UNESCAPE_INPLACE)
				
```

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlunescapea">UrlUnescape</a>