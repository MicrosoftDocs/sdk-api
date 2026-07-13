---
UID: NF:shlwapi.PathIsLFNFileSpecA
title: PathIsLFNFileSpecA function (shlwapi.h)
description: Determines whether a file name is in long format. (ANSI)
helpviewer_keywords: ["PathIsLFNFileSpecA", "shlwapi/PathIsLFNFileSpecA"]
old-location: shell\PathIsLFNFileSpec.htm
tech.root: shell
ms.assetid: 599cb457-da72-4416-bfb7-5bc55a0eeb2d
ms.date: 12/05/2018
ms.keywords: PathIsLFNFileSpec, PathIsLFNFileSpec function [Windows Shell], PathIsLFNFileSpecA, PathIsLFNFileSpecW, _win32_PathIsLFNFileSpec, shell.PathIsLFNFileSpec, shlwapi/PathIsLFNFileSpec, shlwapi/PathIsLFNFileSpecA, shlwapi/PathIsLFNFileSpecW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsLFNFileSpecW (Unicode) and PathIsLFNFileSpecA (ANSI)
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
 - PathIsLFNFileSpecA
 - shlwapi/PathIsLFNFileSpecA
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
 - PathIsLFNFileSpec
 - PathIsLFNFileSpecA
 - PathIsLFNFileSpecW
---

# PathIsLFNFileSpecA function


## -description

Determines whether a file name is in long format.

## -parameters

### -param pszName [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the file name to be tested.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>pszName</i> exceeds the number of characters allowed by the 8.3 format, or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathisfilespeca">PathIsFileSpec</a>

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathIsLFNFileSpec as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
