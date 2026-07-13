---
UID: NF:shlwapi.StrPBrkA
title: StrPBrkA function (shlwapi.h)
description: Searches a string for the first occurrence of a character contained in a specified buffer. This search does not include the terminating null character. (ANSI)
helpviewer_keywords: ["StrPBrkA", "shlwapi/StrPBrkA"]
old-location: shell\StrPBrk.htm
tech.root: shell
ms.assetid: 116c0791-33dd-4c3f-b8a4-a7df91fc5f6a
ms.date: 12/05/2018
ms.keywords: StrPBrk, StrPBrk function [Windows Shell], StrPBrkA, StrPBrkW, _win32_StrPBrk, shell.StrPBrk, shlwapi/StrPBrk, shlwapi/StrPBrkA, shlwapi/StrPBrkW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrPBrkW (Unicode) and StrPBrkA (ANSI)
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
 - StrPBrkA
 - shlwapi/StrPBrkA
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
 - StrPBrk
 - StrPBrkA
 - StrPBrkW
---

# StrPBrkA function


## -description

Searches a string for the first occurrence of a character contained in a specified buffer. This search does not include the terminating null character.

## -parameters

### -param psz [in]

Type: <b>PTSTR</b>

A pointer to the null-terminated string to be searched.

### -param pszSet [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated character buffer that contains the characters for which to search.

## -returns

Type: <b>PTSTR</b>

Returns the address in <i>psz</i> of the first occurrence of a character contained in the buffer at <i>pszSet</i>, or <b>NULL</b> if no match is found.

## -remarks

> [!NOTE]
> The shlwapi.h header defines StrPBrk as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

