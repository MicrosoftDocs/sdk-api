---
UID: NF:shlwapi.PathAppendW
title: PathAppendW function (shlwapi.h)
description: Appends one path to the end of another. (Unicode)
helpviewer_keywords: ["PathAppend", "PathAppend function [Windows Shell]", "PathAppendW", "_win32_PathAppend", "shell.PathAppend", "shlwapi/PathAppend", "shlwapi/PathAppendW"]
old-location: shell\PathAppend.htm
tech.root: shell
ms.assetid: 896737ef-a05c-4f0f-b8b0-56355ae9c2d9
ms.date: 12/05/2018
ms.keywords: PathAppend, PathAppend function [Windows Shell], PathAppendA, PathAppendW, _win32_PathAppend, shell.PathAppend, shlwapi/PathAppend, shlwapi/PathAppendA, shlwapi/PathAppendW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathAppendW (Unicode) and PathAppendA (ANSI)
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
 - PathAppendW
 - shlwapi/PathAppendW
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
 - PathAppend
 - PathAppendA
 - PathAppendW
---

# PathAppendW function


## -description

Appends one path to the end of another.
        
            
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend">PathCchAppend</a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex">PathCchAppendEx</a> function in its place.</div><div> </div>

## -parameters

### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string to which the path specified in <i>pszMore</i> is appended. You must set the size of this buffer to MAX_PATH to ensure that it is large enough to hold the returned string.

### -param pszMore [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be appended.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

This function automatically inserts a backslash between the two strings, if one is not already present.

The path supplied in <i>pszPath</i> cannot begin with "..\\" or ".\\" to produce a relative path string. If present, those periods are stripped from the output string. For example, appending "path3" to "..\\path1\\path2" results in an output of "\path1\path2\path3" rather than "..\path1\path2\path3".


#### Examples




```cpp

#include <windows.h>
#include <iostream>
#include "Shlwapi.h"

using namespace std;

int main( void )
{
	// String for path name.
	char buffer_1[MAX_PATH] = "name_1\\name_2";
	char *lpStr1;
	lpStr1 = buffer_1;

	// String of what is being added.
	char buffer_2[ ] = "name_3";
	char *lpStr2;
	lpStr2 = buffer_2;

	cout << "The original path string is    " << lpStr1 << endl;
	cout << "The part to append to end is   " << lpStr2 << endl;
	bool ret = PathAppend(lpStr1,lpStr2);
	cout << "The appended path string is    " << lpStr1 << endl;
}

OUTPUT:
--------- 
The original path string is    name_1\name_2
The part to append to end is   name_3
The appended path string is    name_1\name_2\name_3
```





> [!NOTE]
> The shlwapi.h header defines PathAppend as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
