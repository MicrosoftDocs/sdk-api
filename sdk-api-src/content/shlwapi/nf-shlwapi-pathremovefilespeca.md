---
UID: NF:shlwapi.PathRemoveFileSpecA
title: PathRemoveFileSpecA function (shlwapi.h)
description: Removes the trailing file name and backslash from a path, if they are present. (ANSI)
helpviewer_keywords: ["PathRemoveFileSpecA", "shlwapi/PathRemoveFileSpecA"]
old-location: shell\PathRemoveFileSpec.htm
tech.root: shell
ms.assetid: c47bcf8a-c59d-4d6a-81a9-a3960ae39867
ms.date: 12/05/2018
ms.keywords: PathRemoveFileSpec, PathRemoveFileSpec function [Windows Shell], PathRemoveFileSpecA, PathRemoveFileSpecW, _win32_PathRemoveFileSpec, shell.PathRemoveFileSpec, shlwapi/PathRemoveFileSpec, shlwapi/PathRemoveFileSpecA, shlwapi/PathRemoveFileSpecW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathRemoveFileSpecW (Unicode) and PathRemoveFileSpecA (ANSI)
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
 - PathRemoveFileSpecA
 - shlwapi/PathRemoveFileSpecA
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
 - PathRemoveFileSpec
 - PathRemoveFileSpecA
 - PathRemoveFileSpecW
---

# PathRemoveFileSpecA function


## -description

Removes the trailing file name and backslash from a path, if they are present.
<div class="alert"><b>Note</b>  This function is deprecated. We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec">PathCchRemoveFileSpec</a> function in its place.</div><div> </div>

## -parameters

### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path from which to remove the file name.

## -returns

Type: <b>BOOL</b>

Returns nonzero if something was removed, or zero otherwise.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathRemoveFileSpec as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
