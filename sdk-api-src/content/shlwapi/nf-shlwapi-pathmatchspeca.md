---
UID: NF:shlwapi.PathMatchSpecA
title: PathMatchSpecA function (shlwapi.h)
description: Searches a string using a Microsoft MS-DOS wildcard match type. (ANSI)
helpviewer_keywords: ["PathMatchSpecA", "shlwapi/PathMatchSpecA"]
old-location: shell\PathMatchSpec.htm
tech.root: shell
ms.assetid: 908e7204-d168-4179-9c7b-ad46ba68bebc
ms.date: 12/05/2018
ms.keywords: PathMatchSpec, PathMatchSpec function [Windows Shell], PathMatchSpecA, PathMatchSpecW, _win32_PathMatchSpec, shell.PathMatchSpec, shlwapi/PathMatchSpec, shlwapi/PathMatchSpecA, shlwapi/PathMatchSpecW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathMatchSpecW (Unicode) and PathMatchSpecA (ANSI)
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
 - PathMatchSpecA
 - shlwapi/PathMatchSpecA
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
 - PathMatchSpec
 - PathMatchSpecA
 - PathMatchSpecW
---

# PathMatchSpecA function


## -description

Searches a string using a Microsoft MS-DOS wildcard match type.

## -parameters

### -param pszFile [in]

Type: <b>LPCSTR</b>

A pointer to a null-terminated string that contains the path to be searched.

### -param pszSpec [in]

Type: <b>LPCSTR</b>

A pointer to a null-terminated string that contains the file type for which to search. For example, to test whether <i>pszFile</i> is a .doc file, <i>pszSpec</i> should be set to "*.doc".

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the string matches, or <b>FALSE</b> otherwise.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathMatchSpec as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

