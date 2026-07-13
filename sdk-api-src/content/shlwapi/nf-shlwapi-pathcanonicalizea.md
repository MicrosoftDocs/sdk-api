---
UID: NF:shlwapi.PathCanonicalizeA
title: PathCanonicalizeA function (shlwapi.h)
description: Simplifies a path by removing navigation elements such as &quot;.&quot; and &quot;..&quot; to produce a direct, well-formed path. (ANSI)
helpviewer_keywords: ["PathCanonicalizeA", "shlwapi/PathCanonicalizeA"]
old-location: shell\PathCanonicalize.htm
tech.root: shell
ms.assetid: e9b1e877-2cd6-4dd9-a15b-676cb940daed
ms.date: 12/05/2018
ms.keywords: PathCanonicalize, PathCanonicalize function [Windows Shell], PathCanonicalizeA, PathCanonicalizeW, _win32_PathCanonicalize, shell.PathCanonicalize, shlwapi/PathCanonicalize, shlwapi/PathCanonicalizeA, shlwapi/PathCanonicalizeW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathCanonicalizeW (Unicode) and PathCanonicalizeA (ANSI)
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
 - PathCanonicalizeA
 - shlwapi/PathCanonicalizeA
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
 - PathCanonicalize
 - PathCanonicalizeA
 - PathCanonicalizeW
---

# PathCanonicalizeA function


## -description

Simplifies a path by removing navigation elements such as "." and ".." to produce a direct, well-formed path.
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize">PathCchCanonicalize</a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalizeex">PathCchCanonicalizeEx</a> function in its place.</div><div> </div>

## -parameters

### -param pszBuf [out]

Type: <b>LPTSTR</b>

A pointer to a string that receives the canonicalized path. You must set the size of this buffer to MAX_PATH to ensure that it is large enough to hold the returned string.

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be canonicalized.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if a result has been computed and the content of the <i>lpszDst</i> output buffer is valid. Returns <b>FALSE</b> otherwise, and the contents of the buffer pointed to by <i>lpszDst</i> are invalid. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function allows the user to specify what to remove from a path by inserting special character sequences into the path. The ".." sequence indicates to remove a path segment from the current position to the previous path segment. The "." sequence indicates to skip over the next path segment to the following path segment. The root segment of the path cannot be removed.

If there are more ".." sequences than there are path segments, the function returns <b>TRUE</b> and contents of the buffer pointed to by <i>lpszDst</i> contains just the root, "\".


#### Examples




```cpp

#include <windows.h>
#include <iostream>
#include "Shlwapi.h"

using namespace std;

int main( void )
{
// Path_1 destination buffer.
char buffer_1[MAX_PATH] = "JustABufferToHoldTheCanonicalizedPathForAnExample";
char *lpStr1;
lpStr1 = buffer_1;

// Path_2 to be Canonicalized.
char buffer_2[ ] = "A:\\name_1\\.\\name_2\\..\\name_3";
char *lpStr2;
lpStr2 = buffer_2;

// Path_3 to be Canonicalized.
char buffer_3[ ] = "A:\\name_1\\..\\name_2\\.\\name_3";
char *lpStr3;
lpStr3 = buffer_3;

// Path_4 to be Canonicalized.
char buffer_4[ ] = "A:\\name_1\\name_2\\.\\name_3\\..\\name_4";
char *lpStr4;
lpStr4 = buffer_4;

// Path_5 to be Canonicalized.
char buffer_5[ ] = "A:\\name_1\\.\\name_2\\.\\name_3\\..\\name_4\\..";
char *lpStr5;
lpStr5 = buffer_5;

// Path_6 to be Canonicalized.
char buffer_6[ ] = "C:\\..";
char *lpStr6;
lpStr6 = buffer_6;

cout << "The un-canonicalized path 2 is : " << lpStr2
     << "\nThe return value is            : " 
     << PathCanonicalize(lpStr1,lpStr2)
     << "\nThe canonicalized path 1 is    : " << lpStr1 << endl;

cout << "\nThe un-canonicalized path 3 is : " << lpStr3
     << "\nThe return value is            : " 
     << PathCanonicalize(lpStr1,lpStr3)
     << "\nThe canonicalized path 1 is    : " << lpStr1 << endl;

cout << "\nThe un-canonicalized path 4 is : " << lpStr4
     << "\nThe return value is            : " 
     << PathCanonicalize(lpStr1,lpStr4)
     << "\nThe canonicalized path 1 is    : " << lpStr1 << endl;

cout << "\nThe un-canonicalized path 5 is : " << lpStr5
     << "\nThe return value is            : " 
     << PathCanonicalize(lpStr1,lpStr5) 
     << "\nThe canonicalized path 1 is    : " << lpStr1 << endl;

cout << "\nThe un-canonicalized path 6 is : " << lpStr6
     << "\nThe return value is            : " 
     << PathCanonicalize(lpStr1,lpStr6)
     << "\nThe canonicalized path 1 is    : " << lpStr1 << endl;
}
OUTPUT:
---------
The un-canonicalized path 2 is : A:\name_1\.\name_2\..\name_3
The return value is            : 1
The canonicalized path 1 is    : A:\name_1\name_3

The un-canonicalized path 3 is : A:\name_1\..\name_2\.\name_3
The return value is            : 1
The canonicalized path 1 is    : A:\name_2\name_3

The un-canonicalized path 4 is : A:\name_1\name_2\.\name_3\..\name_4
The return value is            : 1
The canonicalized path 1 is    : A:\name_1\name_2\name_4

The un-canonicalized path 5 is : A:\name_1\.\name_2\.\name_3\..\name_4\..
The return value is            : 1
The canonicalized path 1 is    : A:\name_1\name_2

The un-canonicalized path 6 is : C:\..
The return value is            : 1
The canonicalized path 1 is    : C:\
```





> [!NOTE]
> The shlwapi.h header defines PathCanonicalize as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
