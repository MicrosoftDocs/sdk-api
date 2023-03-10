---
UID: NF:shlwapi.UrlIsNoHistoryW
title: UrlIsNoHistoryW function (shlwapi.h)
description: Returns whether a URL is a URL that browsers typically do not include in navigation history. (Unicode)
helpviewer_keywords: ["UrlIsNoHistory", "UrlIsNoHistory function [Windows Shell]", "UrlIsNoHistoryW", "_win32_UrlIsNoHistory", "shell.UrlIsNoHistory", "shlwapi/UrlIsNoHistory", "shlwapi/UrlIsNoHistoryW"]
old-location: shell\UrlIsNoHistory.htm
tech.root: shell
ms.assetid: 7602d2ef-1f21-4b2f-8ac9-195bb21d6ae7
ms.date: 12/05/2018
ms.keywords: UrlIsNoHistory, UrlIsNoHistory function [Windows Shell], UrlIsNoHistoryA, UrlIsNoHistoryW, _win32_UrlIsNoHistory, shell.UrlIsNoHistory, shlwapi/UrlIsNoHistory, shlwapi/UrlIsNoHistoryA, shlwapi/UrlIsNoHistoryW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlIsNoHistoryW (Unicode) and UrlIsNoHistoryA (ANSI)
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
 - UrlIsNoHistoryW
 - shlwapi/UrlIsNoHistoryW
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
 - UrlIsNoHistory
 - UrlIsNoHistoryA
 - UrlIsNoHistoryW
---

# UrlIsNoHistoryW function


## -description

Returns whether a URL is a URL that browsers typically do not include in navigation history.

## -parameters

### -param pszURL [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.

## -returns

Type: <b>BOOL</b>

Returns a nonzero value if the URL is a URL that is not included in navigation history, or zero otherwise.

## -remarks

This function is equivalent to the following:
				
                


``` syntax
UrlIs(pszURL, URLIS_NOHISTORY)
```


## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlisa">UrlIs</a>
