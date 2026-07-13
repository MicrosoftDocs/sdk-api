---
UID: NF:shlwapi.PathFindExtensionW
title: PathFindExtensionW function (shlwapi.h)
description: Searches a path for an extension. (Unicode)
helpviewer_keywords: ["PathFindExtension", "PathFindExtension function [Windows Shell]", "PathFindExtensionW", "_win32_PathFindExtension", "shell.PathFindExtension", "shlwapi/PathFindExtension", "shlwapi/PathFindExtensionW"]
old-location: shell\PathFindExtension.htm
tech.root: shell
ms.assetid: afebd4b7-2685-4b6e-8f8a-d43944dacef5
ms.date: 12/05/2018
ms.keywords: PathFindExtension, PathFindExtension function [Windows Shell], PathFindExtensionA, PathFindExtensionW, _win32_PathFindExtension, shell.PathFindExtension, shlwapi/PathFindExtension, shlwapi/PathFindExtensionA, shlwapi/PathFindExtensionW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathFindExtensionW (Unicode) and PathFindExtensionA (ANSI)
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
 - PathFindExtensionW
 - shlwapi/PathFindExtensionW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathFindExtension
 - PathFindExtensionA
 - PathFindExtensionW
---

# PathFindExtensionW function


## -description

Searches a path for an extension.

## -parameters

### -param pszPath [in]

Type: <b>PTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to search, including the extension being searched for.

## -returns

Type: <b>PTSTR</b>

Returns the address of the "." that precedes the extension within <i>pszPath</i> if an extension is found, or the address of the terminating null character otherwise.

## -remarks

Note that a valid file name extension cannot contain a space. For more information on valid file name extensions, see <a href="/windows/desktop/shell/fa-file-extensions">File Type Handlers</a>.




> [!NOTE]
> The shlwapi.h header defines PathFindExtension as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
