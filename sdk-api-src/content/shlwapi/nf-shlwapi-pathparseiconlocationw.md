---
UID: NF:shlwapi.PathParseIconLocationW
title: PathParseIconLocationW function (shlwapi.h)
description: Parses a file location string that contains a file location and icon index, and returns separate values. (Unicode)
helpviewer_keywords: ["PathParseIconLocation", "PathParseIconLocation function [Windows Shell]", "PathParseIconLocationW", "_win32_PathParseIconLocation", "shell.PathParseIconLocation", "shlwapi/PathParseIconLocation", "shlwapi/PathParseIconLocationW"]
old-location: shell\PathParseIconLocation.htm
tech.root: shell
ms.assetid: 1ded2f0f-0e11-4730-ab7b-16536e7f4435
ms.date: 12/05/2018
ms.keywords: PathParseIconLocation, PathParseIconLocation function [Windows Shell], PathParseIconLocationA, PathParseIconLocationW, _win32_PathParseIconLocation, shell.PathParseIconLocation, shlwapi/PathParseIconLocation, shlwapi/PathParseIconLocationA, shlwapi/PathParseIconLocationW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathParseIconLocationW (Unicode) and PathParseIconLocationA (ANSI)
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
 - PathParseIconLocationW
 - shlwapi/PathParseIconLocationW
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
 - PathParseIconLocation
 - PathParseIconLocationA
 - PathParseIconLocationW
---

# PathParseIconLocationW function


## -description

Parses a file location string that contains a file location and icon index, and returns separate values.

## -parameters

### -param pszIconFile [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains a file location string. It should be in the form "<i>path</i>,<i>iconindex</i>". When the function returns, <i>pszIconFile</i> will point to the file's path.

## -returns

Type: <b>int</b>

Returns the valid icon index value.

## -remarks

This function is useful for taking a DefaultIcon value retrieved from the registry by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shgetvaluea">SHGetValue</a> and separating the icon index from the path.


#### Examples




```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main(void)
{
// Path to parse for file and icon index.
char buffer_1[ ] = "C:\\TEST\\sample.txt,3"; 
char *lpStr1;
lpStr1 = buffer_1;

// Return value from "PathParseIconLocation".
int retval;

// Search a path to parse for file and icon index.
retval = PathParseIconLocation(lpStr1);
cout << "The path to parse for file and icon index is   : " << lpStr1 << endl;
cout << "PathParseIconLocation returns the icon index of: " << retval << endl;
}

OUTPUT:
==========
The path to parse for file and icon index is   : C:\TEST\sample.txt
PathParseIconLocation returns the icon index of: 3
```





> [!NOTE]
> The shlwapi.h header defines PathParseIconLocation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
