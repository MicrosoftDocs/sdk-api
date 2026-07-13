---
UID: NF:shlwapi.PathAddExtensionA
title: PathAddExtensionA function (shlwapi.h)
description: Adds a file name extension to a path string. (ANSI)
helpviewer_keywords: ["PathAddExtensionA", "shlwapi/PathAddExtensionA"]
old-location: shell\PathAddExtension.htm
tech.root: shell
ms.assetid: 2c113d11-11d5-4362-bad5-c859d65aca2a
ms.date: 12/05/2018
ms.keywords: PathAddExtension, PathAddExtension function [Windows Shell], PathAddExtensionA, PathAddExtensionW, _win32_PathAddExtension, shell.PathAddExtension, shlwapi/PathAddExtension, shlwapi/PathAddExtensionA, shlwapi/PathAddExtensionW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathAddExtensionW (Unicode) and PathAddExtensionA (ANSI)
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
 - PathAddExtensionA
 - shlwapi/PathAddExtensionA
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
 - PathAddExtension
 - PathAddExtensionA
 - PathAddExtensionW
---

# PathAddExtensionA function


## -description

Adds a file name extension to a path string.
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension">PathCchAddExtension</a> function in its place.</div><div> </div>

## -parameters

### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a buffer with the null-terminated string to which the file name extension will be appended. You must set the size of this buffer to MAX_PATH to ensure that it is large enough to hold the returned string.

### -param pszExt [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the file name extension. This value can be <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if an extension was added, or <b>FALSE</b> otherwise.

## -remarks

If there is already a file name extension present, no extension will be added. If the <i>pszPath</i> points to a <b>NULL</b> string, the result will be the file name extension only. If <i>pszExtension</i> points to a <b>NULL</b> string, an ".exe" extension will be added.


#### Examples


```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main( void )
{
     // String for path name without file name extension.
     char buffer_1[MAX_PATH] = "file";
     char *lpStr1;
     lpStr1 = buffer_1;

     // String for path name with file name extension.
     char buffer_2[ ] = "file.doc";
     char *lpStr2;
     lpStr2 = buffer_2;

     // String for extension name.
     char F_Ext[MAX_PATH] = ".txt";
     char *lpStr3;
     lpStr3 = F_Ext;

     // Null string as path. 
     char N_String[MAX_PATH] = "\0";
     char *lpStr4;
     lpStr4 = N_String;

     // Path 1 without the file name extension.
     cout << "The original path string 1 is  " << lpStr1 << endl;

     int ret_1 = PathAddExtension(lpStr1,lpStr3);
     cout << "The modified path string 1 is  " << lpStr1 << endl;

    // Path 2 with the file name extension already there.
    cout << "The original path string 2 is  " << lpStr2 << endl;
    int ret_2 = PathAddExtension(lpStr2,lpStr3);
    cout << "The modified path string 2 is  " << lpStr2<< endl;

    // Path 3 null string as a path.
    int ret_3 = PathAddExtension(lpStr4,lpStr3);
    cout << "The return value is " << ret_3<< endl;
    cout << "The modified path on a null string is " << lpStr4<< endl;

}

OUTPUT:
-----------------------
The original path string 1 is  file
The modified path string 1 is  file.txt
The original path string 2 is  file.doc
The modified path string 2 is  file.doc
The return value is 1
The modified path on a null string is .txt
The return value is 1
```





> [!NOTE]
> The shlwapi.h header defines PathAddExtension as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
