---
UID: NF:shlwapi.PathRemoveArgsW
title: PathRemoveArgsW function (shlwapi.h)
description: Removes any arguments from a given path. (Unicode)
helpviewer_keywords: ["PathRemoveArgs", "PathRemoveArgs function [Windows Shell]", "PathRemoveArgsW", "_win32_PathRemoveArgs", "shell.PathRemoveArgs", "shlwapi/PathRemoveArgs", "shlwapi/PathRemoveArgsW"]
old-location: shell\PathRemoveArgs.htm
tech.root: shell
ms.assetid: 430072bc-4ddc-4b3d-bf32-fb60d7b56faf
ms.date: 12/05/2018
ms.keywords: PathRemoveArgs, PathRemoveArgs function [Windows Shell], PathRemoveArgsA, PathRemoveArgsW, _win32_PathRemoveArgs, shell.PathRemoveArgs, shlwapi/PathRemoveArgs, shlwapi/PathRemoveArgsA, shlwapi/PathRemoveArgsW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathRemoveArgsW (Unicode) and PathRemoveArgsA (ANSI)
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
 - PathRemoveArgsW
 - shlwapi/PathRemoveArgsW
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
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - PathRemoveArgs
 - PathRemoveArgsA
 - PathRemoveArgsW
---

# PathRemoveArgsW function


## -description

Removes any arguments from a given path.

## -parameters

### -param pszPath [in, out]

Type: <b>LPTSTR</b>

Pointer to a null-terminated string of length MAX_PATH that contains the path from which to remove arguments.

## -remarks

This function should not be used on generic command path templates (from users or the registry), but rather it should be used only on templates that the application knows to be well formed.


#### Examples


```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main( void )
{
    // Path with arguments.
    char buffer_1[ ] = "c:\\a\\b\\FileA Arg1 Arg2"; 
    char *lpStr1;
    lpStr1 = buffer_1;
    
    // Path before "PathRemoveArgs".
    cout << "Path before calling \"PathRemoveArgs\": " << lpStr1 << endl;
    
    // Call function "PathRemoveArgs".
    PathRemoveArgs(lpStr1);
    
    // Path after "PathRemoveArgs".
    cout << "Path after calling \"PathRemoveArgs\": " << lpStr1 << endl;
}

OUTPUT:
==================
Path before calling "PathRemoveArgs": c:\a\b\FileA Arg1 Arg2
Path after calling "PathRemoveArgs": c:\a\b\FileA
```





> [!NOTE]
> The shlwapi.h header defines PathRemoveArgs as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

