---
UID: NF:shlwapi.PathIsRootA
title: PathIsRootA function (shlwapi.h)
description: Determines whether a path string refers to the root of a volume. (ANSI)
helpviewer_keywords: ["PathIsRootA", "shlwapi/PathIsRootA"]
old-location: shell\PathIsRoot.htm
tech.root: shell
ms.assetid: 8586df98-91c4-49a6-9b07-7dceb8a63431
ms.date: 12/05/2018
ms.keywords: PathIsRoot, PathIsRoot function [Windows Shell], PathIsRootA, PathIsRootW, _win32_PathIsRoot, shell.PathIsRoot, shlwapi/PathIsRoot, shlwapi/PathIsRootA, shlwapi/PathIsRootW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsRootW (Unicode) and PathIsRootA (ANSI)
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
 - PathIsRootA
 - shlwapi/PathIsRootA
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
 - PathIsRoot
 - PathIsRootA
 - PathIsRootW
---

# PathIsRootA function


## -description

Determines whether a path string refers to the root of a volume.

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be validated.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the specified path is a root, or <b>FALSE</b> otherwise.

## -remarks

Returns <b>TRUE</b> for paths such as "\", "<i>X</i>:\" or "&#92;&#92;<i>server</i>&#92;<i>share</i>". Paths such as "..\path2" or "&#92;&#92;<i>server</i>\" return <b>FALSE</b>.
            


#### Examples




```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main( void )
{
// String path name 1.
char buffer_1[ ] = "C:\\";
char *lpStr1;
lpStr1 = buffer_1;

// String path name 2.
char buffer_2[ ] = "path\\file";
char *lpStr2;
lpStr2 = buffer_2;

// Variable to get the return from "PathIsRoot".
int retval;

// Test case with path not absolute.
retval = PathIsRoot(lpStr1);
cout << "The return from function is       :" << retval << endl;
cout << "The path does contain a root part :" << lpStr1 << endl;

// Test case with path absolute.
retval = PathIsRoot(lpStr2);
cout << "The return from function is       :" << retval << endl;
cout << "The path does not contain part    :" << lpStr2 << endl;
}

OUTPUT:
============
The return from function is       :1
The path does contain a root part :C:\
The return from function is       :0
The path does not contain part    :path\file
============
```





> [!NOTE]
> The shlwapi.h header defines PathIsRoot as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

