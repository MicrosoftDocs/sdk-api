---
UID: NF:shlwapi.StrTrimW
title: StrTrimW function (shlwapi.h)
description: Removes specified leading and trailing characters from a string. (Unicode)
helpviewer_keywords: ["StrTrim", "StrTrim function [Windows Shell]", "StrTrimW", "_win32_StrTrim", "shell.StrTrim", "shlwapi/StrTrim", "shlwapi/StrTrimW"]
old-location: shell\StrTrim.htm
tech.root: shell
ms.assetid: aea422b9-326e-4b12-b2a9-7c220677a467
ms.date: 12/05/2018
ms.keywords: StrTrim, StrTrim function [Windows Shell], StrTrimA, StrTrimW, _win32_StrTrim, shell.StrTrim, shlwapi/StrTrim, shlwapi/StrTrimA, shlwapi/StrTrimW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrTrimW (Unicode) and StrTrimA (ANSI)
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
 - StrTrimW
 - shlwapi/StrTrimW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - StrTrim
 - StrTrimA
 - StrTrimW
---

# StrTrimW function


## -description

Removes specified leading and trailing characters from a string.

## -parameters

### -param psz [in, out]

Type: <b>PTSTR</b>

A pointer to the null-terminated string to be trimmed. When this function returns successfully, <i>psz</i> receives the trimmed string.

### -param pszTrimChars [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string that contains the characters to trim from <i>psz</i>.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if any characters were removed; otherwise, <b>FALSE</b>.

## -remarks

> [!NOTE]
> The shlwapi.h header defines StrTrim as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

