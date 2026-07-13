---
UID: NF:shlwapi.PathStripPathW
title: PathStripPathW function (shlwapi.h)
description: Removes the path portion of a fully qualified path and file. (Unicode)
helpviewer_keywords: ["PathStripPath", "PathStripPath function [Windows Shell]", "PathStripPathW", "_win32_PathStripPath", "shell.PathStripPath", "shlwapi/PathStripPath", "shlwapi/PathStripPathW"]
old-location: shell\PathStripPath.htm
tech.root: shell
ms.assetid: 84b439f2-f570-4e7f-bc3f-e0fdd185ea15
ms.date: 12/05/2018
ms.keywords: PathStripPath, PathStripPath function [Windows Shell], PathStripPathA, PathStripPathW, _win32_PathStripPath, shell.PathStripPath, shlwapi/PathStripPath, shlwapi/PathStripPathA, shlwapi/PathStripPathW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathStripPathW (Unicode) and PathStripPathA (ANSI)
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
 - PathStripPathW
 - shlwapi/PathStripPathW
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
 - PathStripPath
 - PathStripPathA
 - PathStripPathW
---

# PathStripPathW function


## -description

Removes the path portion of a fully qualified path and file.

## -parameters

### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path and file name. When this function returns successfully, the string contains only the file name, with the path removed.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathStripPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

