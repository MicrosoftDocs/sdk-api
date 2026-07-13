---
UID: NF:shlwapi.PathQuoteSpacesA
title: PathQuoteSpacesA function (shlwapi.h)
description: Searches a path for spaces. If spaces are found, the entire path is enclosed in quotation marks. (ANSI)
helpviewer_keywords: ["PathQuoteSpacesA", "shlwapi/PathQuoteSpacesA"]
old-location: shell\PathQuoteSpaces.htm
tech.root: shell
ms.assetid: 76a51c21-b924-4919-a6bb-8c6bdec5b3f0
ms.date: 12/05/2018
ms.keywords: PathQuoteSpaces, PathQuoteSpaces function [Windows Shell], PathQuoteSpacesA, PathQuoteSpacesW, _win32_PathQuoteSpaces, shell.PathQuoteSpaces, shlwapi/PathQuoteSpaces, shlwapi/PathQuoteSpacesA, shlwapi/PathQuoteSpacesW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathQuoteSpacesW (Unicode) and PathQuoteSpacesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathQuoteSpacesA
 - shlwapi/PathQuoteSpacesA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-shlwapi-l1-1-0.dll
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathQuoteSpaces
 - PathQuoteSpacesA
 - PathQuoteSpacesW
---

# PathQuoteSpacesA function


## -description

Searches a path for spaces. If spaces are found, the entire path is enclosed in quotation marks.

## -parameters

### -param lpsz [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string that contains the path to search. The size of this buffer must be set to MAX_PATH to ensure that it is large enough to hold the returned string.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if spaces were found; otherwise, <b>FALSE</b>.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathQuoteSpaces as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

