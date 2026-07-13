---
UID: NF:shlwapi.PathSearchAndQualifyW
title: PathSearchAndQualifyW function (shlwapi.h)
description: Determines if a given path is correctly formatted and fully qualified. (Unicode)
helpviewer_keywords: ["PathSearchAndQualify", "PathSearchAndQualify function [Windows Shell]", "PathSearchAndQualifyW", "_win32_PathSearchAndQualify", "shell.PathSearchAndQualify", "shlwapi/PathSearchAndQualify", "shlwapi/PathSearchAndQualifyW"]
old-location: shell\PathSearchAndQualify.htm
tech.root: shell
ms.assetid: 90da281d-349a-460a-aa5a-14e3b4ced727
ms.date: 12/05/2018
ms.keywords: PathSearchAndQualify, PathSearchAndQualify function [Windows Shell], PathSearchAndQualifyA, PathSearchAndQualifyW, _win32_PathSearchAndQualify, shell.PathSearchAndQualify, shlwapi/PathSearchAndQualify, shlwapi/PathSearchAndQualifyA, shlwapi/PathSearchAndQualifyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathSearchAndQualifyW (Unicode) and PathSearchAndQualifyA (ANSI)
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
 - PathSearchAndQualifyW
 - shlwapi/PathSearchAndQualifyW
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
 - PathSearchAndQualify
 - PathSearchAndQualifyA
 - PathSearchAndQualifyW
---

# PathSearchAndQualifyW function


## -description

Determines if a given path is correctly formatted and fully qualified.

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to search.

### -param pszBuf [out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be referenced.

### -param cchBuf [in]

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszFullyQualifiedPath</i>, in characters.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the path is qualified, or <b>FALSE</b> otherwise.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathSearchAndQualify as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

