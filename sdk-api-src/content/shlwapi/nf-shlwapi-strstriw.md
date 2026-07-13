---
UID: NF:shlwapi.StrStrIW
title: StrStrIW function (shlwapi.h)
description: Finds the first occurrence of a substring within a string. The comparison is not case-sensitive. (Unicode)
helpviewer_keywords: ["StrStrI", "StrStrI function [Windows Shell]", "StrStrIW", "_win32_StrStrI", "shell.StrStrI", "shlwapi/StrStrI", "shlwapi/StrStrIW"]
old-location: shell\StrStrI.htm
tech.root: shell
ms.assetid: b0281641-1375-4815-a707-03e1ce7e5a29
ms.date: 12/05/2018
ms.keywords: StrStrI, StrStrI function [Windows Shell], StrStrIA, StrStrIW, _win32_StrStrI, shell.StrStrI, shlwapi/StrStrI, shlwapi/StrStrIA, shlwapi/StrStrIW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrStrIW (Unicode) and StrStrIA (ANSI)
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
 - StrStrIW
 - shlwapi/StrStrIW
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
 - StrStrI
 - StrStrIA
 - StrStrIW
---

# StrStrIW function


## -description

Finds the first occurrence of a substring within a string. The comparison is not case-sensitive.

## -parameters

### -param pszFirst [in]

Type: <b>PTSTR</b>

A pointer to the null-terminated string being searched.

### -param pszSrch [in]

Type: <b>PCTSTR</b>

A pointer to the substring to search for.

## -returns

Type: <b>PTSTR</b>

Returns the address of the first occurrence of the matching substring if successful, or <b>NULL</b> otherwise.

## -remarks

> [!NOTE]
> The shlwapi.h header defines StrStrI as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

