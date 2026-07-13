---
UID: NF:shlwapi.PathCompactPathExA
title: PathCompactPathExA function (shlwapi.h)
description: Truncates a path to fit within a certain number of characters by replacing path components with ellipses. (ANSI)
helpviewer_keywords: ["PathCompactPathExA", "shlwapi/PathCompactPathExA"]
old-location: shell\PathCompactPathEx.htm
tech.root: shell
ms.assetid: ff108ee6-3d71-4ab2-a04a-d4bcce408f88
ms.date: 12/05/2018
ms.keywords: PathCompactPathEx, PathCompactPathEx function [Windows Shell], PathCompactPathExA, PathCompactPathExW, _win32_PathCompactPathEx, shell.PathCompactPathEx, shlwapi/PathCompactPathEx, shlwapi/PathCompactPathExA, shlwapi/PathCompactPathExW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathCompactPathExW (Unicode) and PathCompactPathExA (ANSI)
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
 - PathCompactPathExA
 - shlwapi/PathCompactPathExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - PathCompactPathEx
 - PathCompactPathExA
 - PathCompactPathExW
---

# PathCompactPathExA function


## -description

Truncates a path to fit within a certain number of characters by replacing path components with ellipses.

## -parameters

### -param pszOut [out]

Type: <b>LPTSTR</b>

The address of the string that has been altered.

### -param pszSrc [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be altered.

### -param cchMax [in]

Type: <b>UINT</b>

The maximum number of characters to be contained in the new string, including the terminating null character. For example, if <i>cchMax</i> = 8, the resulting string can contain a maximum of 7 characters plus the terminating null character.

### -param dwFlags [in]

Type: <b>DWORD</b>

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

The '/' separator will be used instead of '\' if the original string used it. If <i>pszSrc</i> points to a file name that is too long, instead of a path, the file name will be truncated to <i>cchMax</i> characters, including the ellipsis and the terminating <b>NULL</b> character. For example, if the input file name is "My Filename" and <i>cchMax</i> is 10, <b>PathCompactPathEx</b> will return "My Fil...".




> [!NOTE]
> The shlwapi.h header defines PathCompactPathEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

