---
UID: NF:shlwapi.PathGetArgsW
title: PathGetArgsW function (shlwapi.h)
description: Finds the command line arguments within a given path. (Unicode)
helpviewer_keywords: ["PathGetArgs", "PathGetArgs function [Windows Shell]", "PathGetArgsW", "_win32_PathGetArgs", "shell.PathGetArgs", "shlwapi/PathGetArgs", "shlwapi/PathGetArgsW"]
old-location: shell\PathGetArgs.htm
tech.root: shell
ms.assetid: 17dfb601-1306-41b6-a504-8bf69ff204c9
ms.date: 12/05/2018
ms.keywords: PathGetArgs, PathGetArgs function [Windows Shell], PathGetArgsA, PathGetArgsW, _win32_PathGetArgs, shell.PathGetArgs, shlwapi/PathGetArgs, shlwapi/PathGetArgsA, shlwapi/PathGetArgsW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathGetArgsW (Unicode) and PathGetArgsA (ANSI)
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
 - PathGetArgsW
 - shlwapi/PathGetArgsW
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
 - PathGetArgs
 - PathGetArgsA
 - PathGetArgsW
---

# PathGetArgsW function


## -description

Finds the command line arguments within a given path.

## -parameters

### -param pszPath [in]

Type: <b>PTSTR</b>

Pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be searched.

## -returns

Type: <b>PTSTR</b>

Returns a pointer to a null-terminated string that contains the arguments portion of the path if successful. 

                    

If there are no arguments in the path, the function returns a pointer to the end of the input string.

If the function is given a <b>NULL</b> argument it returns <b>NULL</b>.

## -remarks

This function should not be used on generic command path templates (from users or the registry), but rather should be used only on templates that the application knows to be well formed.


#### Examples


```cpp

#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main( void )
{
    // Path_1 to search for file arguments (2 arguments):
    char buffer_1[ ] = "test.exe temp.txt sample.doc"; 
    char *lpStr1;
    lpStr1 = buffer_1;
    
    // Path_2 to search for file arguments (3 arguments):
    char buffer_2[ ] = "test.exe 1 2 3"; 
    char *lpStr2;
    lpStr2 = buffer_2;
    
    // Path_3 to search for file arguments (3 arguments):
    char buffer_3[ ] = "test.exe sample All 15"; 
    char *lpStr3;
    lpStr3 = buffer_3;
    
    // Path_4 to search for file arguments (no arguments):
    char buffer_4[ ] = "test.exe"; 
    char *lpStr4;
    lpStr4 = buffer_4;
    
    cout << "The path passed to the function was : " << lpStr1 <<
            "\nThe arg(s)found in path 1 were      : " << PathGetArgs(lpStr1) << endl;
    
    cout << "\nThe path passed to the function was : " << lpStr2 <<
            "\nThe arg(s)found in path 2 were      : " << PathGetArgs(lpStr2) << endl;
    
    cout << "\nThe path passed to the function was : " << lpStr3 <<
            "\nThe arg(s)found in path 3 were      : " << PathGetArgs(lpStr3) << endl;
    
    cout << "\nThe path passed to the function was : " << lpStr4 <<
            "\nThe arg(s)found in path 4 were      : " << PathGetArgs(lpStr4) << endl;
}

OUTPUT:
===========
The path passed to the function was : test.exe temp.txt sample.doc
The arg(s)found in path 1 were      : temp.txt sample.doc

The path passed to the function was : test.exe 1 2 3
The arg(s)found in path 2 were      : 1 2 3

The path passed to the function was : test.exe sample All 15
The arg(s)found in path 3 were      : sample All 15

The path passed to the function was : test.exe
The arg(s)found in path 4 were      :
===========
```





> [!NOTE]
> The shlwapi.h header defines PathGetArgs as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

