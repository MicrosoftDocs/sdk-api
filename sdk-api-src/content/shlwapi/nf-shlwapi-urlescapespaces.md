---
UID: NF:shlwapi.UrlEscapeSpaces
title: UrlEscapeSpaces macro (shlwapi.h)
description: A macro that converts space characters into their corresponding escape sequence.
helpviewer_keywords: ["UrlEscapeSpaces","UrlEscapeSpaces function [Windows Shell]","_win32_UrlEscapeSpaces","shell.UrlEscapeSpaces","shlwapi/UrlEscapeSpaces"]
old-location: shell\UrlEscapeSpaces.htm
tech.root: shell
ms.assetid: d6d676f1-0ef3-4701-99b2-ca520b39ce6e
ms.date: 12/05/2018
ms.keywords: UrlEscapeSpaces, UrlEscapeSpaces function [Windows Shell], _win32_UrlEscapeSpaces, shell.UrlEscapeSpaces, shlwapi/UrlEscapeSpaces
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
 - UrlEscapeSpaces
 - shlwapi/UrlEscapeSpaces
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
 - UrlEscapeSpaces
---

# UrlEscapeSpaces macro


## -description

A macro that converts space characters into their corresponding escape sequence.

## -parameters

### -param pszUrl [in]

Type: <b>LPCTSTR</b>

A pointer to a URL string. If it does not refer to a file, it must include a valid scheme such as "http://".

### -param pszEscaped [out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string containing the string pointed to by <i>pszURL</i>, with space characters converted to their escape sequence.

### -param pcchEscaped [out]

Type: <b>LPDWORD</b>

The number of characters in <i>pszEscaped</i>.

## -remarks

<b>UrlEscapeSpaces</b> is equivalent to the following: 

				


```

UrlCanonicalize(pszUrl, 
                pszEscaped, 
                pcchEscaped, 
                URL_ESCAPE_SPACES_ONLY | URL_DONT_ESCAPE_EXTRA_INFO )
				
```

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlcanonicalizea">UrlCanonicalize</a>