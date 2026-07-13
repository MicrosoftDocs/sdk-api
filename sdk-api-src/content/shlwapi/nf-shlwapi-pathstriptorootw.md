---
UID: NF:shlwapi.PathStripToRootW
title: PathStripToRootW function (shlwapi.h)
description: Removes all file and directory elements in a path except for the root information. (Unicode)
helpviewer_keywords: ["PathStripToRoot", "PathStripToRoot function [Windows Shell]", "PathStripToRootW", "_win32_PathStripToRoot", "shell.PathStripToRoot", "shlwapi/PathStripToRoot", "shlwapi/PathStripToRootW"]
old-location: shell\PathStripToRoot.htm
tech.root: shell
ms.assetid: ce9a1a40-2a03-44d2-80bc-0dc10654550b
ms.date: 12/05/2018
ms.keywords: PathStripToRoot, PathStripToRoot function [Windows Shell], PathStripToRootA, PathStripToRootW, _win32_PathStripToRoot, shell.PathStripToRoot, shlwapi/PathStripToRoot, shlwapi/PathStripToRootA, shlwapi/PathStripToRootW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathStripToRootW (Unicode) and PathStripToRootA (ANSI)
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
 - PathStripToRootW
 - shlwapi/PathStripToRootW
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
 - PathStripToRoot
 - PathStripToRootA
 - PathStripToRootW
---

# PathStripToRootW function


## -description

Removes all file and directory elements in a path except for the root information.
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot">PathCchStripToRoot</a> function in its place.</div><div> </div>

## -parameters

### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be converted. When this function returns successfully, this string contains only the root information taken from that path.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if a valid drive letter was found in the path, or <b>FALSE</b> otherwise.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathStripToRoot as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
