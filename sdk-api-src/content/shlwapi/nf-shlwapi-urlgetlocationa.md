---
UID: NF:shlwapi.UrlGetLocationA
title: UrlGetLocationA function (shlwapi.h)
description: Retrieves the location from a URL. (ANSI)
helpviewer_keywords: ["UrlGetLocationA", "shlwapi/UrlGetLocationA"]
old-location: shell\UrlGetLocation.htm
tech.root: shell
ms.assetid: e75bde92-2ca0-4d34-a276-50b4eeceda1c
ms.date: 12/05/2018
ms.keywords: UrlGetLocation, UrlGetLocation function [Windows Shell], UrlGetLocationA, UrlGetLocationW, _win32_UrlGetLocation, shell.UrlGetLocation, shlwapi/UrlGetLocation, shlwapi/UrlGetLocationA, shlwapi/UrlGetLocationW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlGetLocationW (Unicode) and UrlGetLocationA (ANSI)
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
 - UrlGetLocationA
 - shlwapi/UrlGetLocationA
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
 - UrlGetLocation
 - UrlGetLocationA
 - UrlGetLocationW
---

# UrlGetLocationA function


## -description

Retrieves the location from a URL.

## -parameters

### -param pszURL [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the location.

## -returns

Type: <b>LPCTSTR</b>

Returns a pointer to a null-terminated string with the location, or <b>NULL</b> otherwise.

## -remarks

The location is the segment of the URL starting with a ? or # character. If a file URL has a query string, the returned string includes the query string.




> [!NOTE]
> The shlwapi.h header defines UrlGetLocation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

