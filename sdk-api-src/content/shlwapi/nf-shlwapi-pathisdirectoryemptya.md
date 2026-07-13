---
UID: NF:shlwapi.PathIsDirectoryEmptyA
title: PathIsDirectoryEmptyA function (shlwapi.h)
description: Determines whether a specified path is an empty directory. (ANSI)
helpviewer_keywords: ["PathIsDirectoryEmptyA", "shlwapi/PathIsDirectoryEmptyA"]
old-location: shell\PathIsDirectoryEmpty.htm
tech.root: shell
ms.assetid: 833fe68e-8b21-4819-8370-d1b5391a3080
ms.date: 12/05/2018
ms.keywords: PathIsDirectoryEmpty, PathIsDirectoryEmpty function [Windows Shell], PathIsDirectoryEmptyA, PathIsDirectoryEmptyW, _win32_PathIsDirectoryEmpty, shell.PathIsDirectoryEmpty, shlwapi/PathIsDirectoryEmpty, shlwapi/PathIsDirectoryEmptyA, shlwapi/PathIsDirectoryEmptyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsDirectoryEmptyW (Unicode) and PathIsDirectoryEmptyA (ANSI)
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
 - PathIsDirectoryEmptyA
 - shlwapi/PathIsDirectoryEmptyA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - ext-ms-win-shell-shlwapi-l1-1-2.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - PathIsDirectoryEmpty
 - PathIsDirectoryEmptyA
 - PathIsDirectoryEmptyW
---

# PathIsDirectoryEmptyA function


## -description

Determines whether a specified path is an empty directory.

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be tested.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>pszPath</i> is an empty directory. Returns <b>FALSE</b> if <i>pszPath</i> is not a directory, or if it contains at least one file other than "." or "..".

## -remarks

"C:\" is considered a directory.





> [!NOTE]
> The shlwapi.h header defines PathIsDirectoryEmpty as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathisdirectorya">PathIsDirectory</a>
