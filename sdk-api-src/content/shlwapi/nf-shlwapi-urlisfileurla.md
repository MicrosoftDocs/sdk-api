---
UID: NF:shlwapi.UrlIsFileUrlA
title: UrlIsFileUrlA macro (shlwapi.h)
description: Tests a URL to determine if it is a file URL. (ANSI)
helpviewer_keywords: ["UrlIsFileUrlA", "shlwapi/UrlIsFileUrlA"]
old-location: shell\UrlIsFileUrl.htm
tech.root: shell
ms.assetid: b122d3e4-47cc-47c0-a30c-6f9d1aa9d174
ms.date: 12/05/2018
ms.keywords: UrlIsFileUrl, UrlIsFileUrl function [Windows Shell], UrlIsFileUrlA, UrlIsFileUrlW, _win32_UrlIsFileUrl, shell.UrlIsFileUrl, shlwapi/UrlIsFileUrl, shlwapi/UrlIsFileUrlA, shlwapi/UrlIsFileUrlW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlIsFileUrlW (Unicode) and UrlIsFileUrlA (ANSI)
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
 - UrlIsFileUrlA
 - shlwapi/UrlIsFileUrlA
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
 - UrlIsFileUrl
 - UrlIsFileUrlA
 - UrlIsFileUrlW
---

# UrlIsFileUrlA macro


## -description

Tests a URL to determine if it is a file URL.

## -parameters

### -param pszURL

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string containing the URL.

## -remarks

A file URL has the form "File://
				<i>xxx</i>". <b>UrlIsFileUrl</b> is actually one of the following macros, depending on whether ANSI or Unicode is selected.
				


```

#define  UrlIsFileUrlA(pszURL) UrlIsA(pszURL, URLIS_FILEURL)
#define  UrlIsFileUrlW(pszURL) UrlIsW(pszURL, URLIS_FILEURL)
				
```






> [!NOTE]
> The shlwapi.h header defines UrlIsFileUrl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlisa">UrlIs</a>
