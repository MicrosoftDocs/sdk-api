---
UID: NF:shlwapi.PathIsDirectoryW
title: PathIsDirectoryW function (shlwapi.h)
description: Verifies that a path is a valid directory. (Unicode)
helpviewer_keywords: ["PathIsDirectory", "PathIsDirectory function [Windows Shell]", "PathIsDirectoryW", "_win32_PathIsDirectory", "shell.PathIsDirectory", "shlwapi/PathIsDirectory", "shlwapi/PathIsDirectoryW"]
old-location: shell\PathIsDirectory.htm
tech.root: shell
ms.assetid: 9af3e3da-6b3a-4e81-ba50-ff7aeeb73c44
ms.date: 12/05/2018
ms.keywords: PathIsDirectory, PathIsDirectory function [Windows Shell], PathIsDirectoryA, PathIsDirectoryW, _win32_PathIsDirectory, shell.PathIsDirectory, shlwapi/PathIsDirectory, shlwapi/PathIsDirectoryA, shlwapi/PathIsDirectoryW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsDirectoryW (Unicode) and PathIsDirectoryA (ANSI)
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
 - PathIsDirectoryW
 - shlwapi/PathIsDirectoryW
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
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
 - Ext-MS-Win-shell-shlwapi-l1-1-0.dll
 - Ext-MS-Win-Shell-ShlwApi-l1-1-1.dll
 - Ext-MS-Win-Shell-ShlwAPI-L1-1-2.dll
api_name:
 - PathIsDirectory
 - PathIsDirectoryA
 - PathIsDirectoryW
---

# PathIsDirectoryW function


## -description

Verifies that a path is a valid directory.

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to verify.

## -returns

Type: <b>BOOL</b>

Returns (BOOL)FILE_ATTRIBUTE_DIRECTORY if the path is a valid directory; otherwise, <b>FALSE</b>.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathIsDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

