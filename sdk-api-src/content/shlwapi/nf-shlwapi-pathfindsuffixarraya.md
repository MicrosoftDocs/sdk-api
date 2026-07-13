---
UID: NF:shlwapi.PathFindSuffixArrayA
title: PathFindSuffixArrayA function (shlwapi.h)
description: Determines whether a given file name has one of a list of suffixes. (ANSI)
helpviewer_keywords: ["PathFindSuffixArrayA", "shlwapi/PathFindSuffixArrayA"]
old-location: shell\PathFindSuffixArray.htm
tech.root: shell
ms.assetid: e2285f7d-bb5d-48c5-bdf1-10ca410389f0
ms.date: 12/05/2018
ms.keywords: PathFindSuffixArray, PathFindSuffixArray function [Windows Shell], PathFindSuffixArrayA, PathFindSuffixArrayW, _win32_PathFindSuffixArray, shell.PathFindSuffixArray, shlwapi/PathFindSuffixArray, shlwapi/PathFindSuffixArrayA, shlwapi/PathFindSuffixArrayW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathFindSuffixArrayW (Unicode) and PathFindSuffixArrayA (ANSI)
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
 - PathFindSuffixArrayA
 - shlwapi/PathFindSuffixArrayA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - PathFindSuffixArray
 - PathFindSuffixArrayA
 - PathFindSuffixArrayW
---

# PathFindSuffixArrayA function


## -description

Determines whether a given file name has one of a list of suffixes.

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the file name to be tested. A full path can be used.

### -param apszSuffix [in]

Type: <b>const LPCTSTR*</b>

An array of <i>iArraySize</i> string pointers. Each string pointed to is null-terminated and contains one suffix. The strings can be of variable lengths.

### -param iArraySize [in]

Type: <b>int</b>

The number of elements in the array pointed to by <i>apszSuffix</i>.

## -returns

Type: <b>LPCTSTR</b>

Returns a pointer to a string with the matching suffix if successful, or <b>NULL</b> if <i>pszPath</i> does not end with one of the specified suffixes.

## -remarks

This function uses a case-sensitive comparison. The suffix must match exactly.




> [!NOTE]
> The shlwapi.h header defines PathFindSuffixArray as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

