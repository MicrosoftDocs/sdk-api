---
UID: NF:shlwapi.PathRemoveBackslashW
title: PathRemoveBackslashW function (shlwapi.h)
description: Removes the trailing backslash from a given path. (Unicode)
helpviewer_keywords: ["PathRemoveBackslash", "PathRemoveBackslash function [Windows Shell]", "PathRemoveBackslashW", "_win32_PathRemoveBackslash", "shell.PathRemoveBackslash", "shlwapi/PathRemoveBackslash", "shlwapi/PathRemoveBackslashW"]
old-location: shell\PathRemoveBackslash.htm
tech.root: shell
ms.assetid: 58d13c38-40aa-4aaa-81dc-2b68425f1fe0
ms.date: 12/05/2018
ms.keywords: PathRemoveBackslash, PathRemoveBackslash function [Windows Shell], PathRemoveBackslashA, PathRemoveBackslashW, _win32_PathRemoveBackslash, shell.PathRemoveBackslash, shlwapi/PathRemoveBackslash, shlwapi/PathRemoveBackslashA, shlwapi/PathRemoveBackslashW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathRemoveBackslashW (Unicode) and PathRemoveBackslashA (ANSI)
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
 - PathRemoveBackslashW
 - shlwapi/PathRemoveBackslashW
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
 - PathRemoveBackslash
 - PathRemoveBackslashA
 - PathRemoveBackslashW
---

# PathRemoveBackslashW function


## -description

Removes the trailing backslash from a given path.
<div class="alert"><b>Note</b>  This function is deprecated. We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash">PathCchRemoveBackslash</a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex">PathCchRemoveBackslashEx</a> function in its place.</div><div> </div>

## -parameters

### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path from which to remove the backslash.

## -returns

Type: <b>LPTSTR</b>

A pointer that, when this function returns successfully and if a backslash has been removed, points to the terminating null character that has replaced the backslash at the end of the string. If the path did not include a trailing backslash, this value will point to the final character in the string.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathRemoveBackslash as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
