---
UID: NF:shlwapi.PathCombineA
title: PathCombineA function (shlwapi.h)
description: Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements. (ANSI)
helpviewer_keywords: ["PathCombineA", "shlwapi/PathCombineA"]
old-location: shell\PathCombine.htm
tech.root: shell
ms.assetid: ed03334b-f688-4993-9685-092135ca29c9
ms.date: 12/05/2018
ms.keywords: PathCombine, PathCombine function [Windows Shell], PathCombineA, PathCombineW, _win32_PathCombine, shell.PathCombine, shlwapi/PathCombine, shlwapi/PathCombineA, shlwapi/PathCombineW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathCombineW (Unicode) and PathCombineA (ANSI)
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
 - PathCombineA
 - shlwapi/PathCombineA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-shlwapi-l1-1-0.dll
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathCombine
 - PathCombineA
 - PathCombineW
---

# PathCombineA function


## -description

Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.
        
            
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine">PathCchCombine</a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex">PathCchCombineEx</a> function in its place.</div><div> </div>

## -parameters

### -param pszDest [out]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the combined path string. You must set the size of this buffer to MAX_PATH to ensure that it is large enough to hold the returned string.

### -param pszDir [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the first path. This value can be <b>NULL</b>.

### -param pszFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the second path. This value can be <b>NULL</b>.

## -returns

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the concatenated path string. This is the same string pointed to by <i>pszPathOut</i>. If this function does not return successfully, this value is <b>NULL</b>.

## -remarks

The directory path should be in the form of A:,B:, ..., Z:. The file path should be in a correct form that represents the file name part of the path. If the directory path ends with a backslash, the backslash will be maintained. Note that while <i>lpszDir</i> and <i>lpszFile</i> are both optional parameters, they cannot both be <b>NULL</b>.


#### Examples




```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main( void )
{
// Buffer to hold combined path.
char buffer_1[MAX_PATH] = "";
char *lpStr1;
lpStr1 = buffer_1;

// String for balance of path name.
char buffer_2[ ] = "One\\Two\\Three";
char *lpStr2;
lpStr2 = buffer_2;

// String for directory name.
char buffer_3[ ] = "C:";
char *lpStr3;
lpStr3 = buffer_3;

cout << "The file path to be combined is  " 
     << lpStr2 << endl;
cout << "The directory name path is       " 
     << lpStr3 << endl;
cout << "The combined path is             " 
     << PathCombine(lpStr1,lpStr3,lpStr2) << endl;
}

------------
INPUT:
------------
Path for directory part: "C:"
Path for file part: "One\Two\Three"
------------
OUTPUT:
------------
The file path to be combined is  One\Two\Three
The directory name path is       C:
The combined path is             C:\One\Two\Three
```





> [!NOTE]
> The shlwapi.h header defines PathCombine as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
