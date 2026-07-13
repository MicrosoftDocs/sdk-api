---
UID: NF:shlwapi.PathCompactPathA
title: PathCompactPathA function (shlwapi.h)
description: Truncates a file path to fit within a given pixel width by replacing path components with ellipses. (ANSI)
helpviewer_keywords: ["PathCompactPathA", "shlwapi/PathCompactPathA"]
old-location: shell\PathCompactPath.htm
tech.root: shell
ms.assetid: b8184c98-1f86-4714-baf8-af4ef3e71cf2
ms.date: 12/05/2018
ms.keywords: PathCompactPath, PathCompactPath function [Windows Shell], PathCompactPathA, PathCompactPathW, _win32_PathCompactPath, shell.PathCompactPath, shlwapi/PathCompactPath, shlwapi/PathCompactPathA, shlwapi/PathCompactPathW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathCompactPathW (Unicode) and PathCompactPathA (ANSI)
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
 - PathCompactPathA
 - shlwapi/PathCompactPathA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - PathCompactPath
 - PathCompactPathA
 - PathCompactPathW
---

# PathCompactPathA function


## -description

Truncates a file path to fit within a given pixel width by replacing path components with ellipses.

## -parameters

### -param hDC [in]

Type: <b>HDC</b>

A handle to the device context used for font metrics. This value can be <b>NULL</b>.

### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be modified. On return, this buffer will contain the modified string.

### -param dx [in]

Type: <b>UINT</b>

The width, in pixels, in which the string must fit.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the path was successfully compacted to the specified width. Returns <b>FALSE</b> on failure, or if the base portion of the path would not fit the specified width.

## -remarks

This function uses the font currently selected in <i>hDC</i> to calculate the width of the text. This function will not compact the path beyond the base file name preceded by ellipses.


#### Examples




```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

HDC hdc;  /* display DC handle to current font metrics */ 

void main( void )
{
// String path name 1.
char buffer_1[MAX_PATH] = "C:\\path1\\path2\\sample.txt";
char *lpStr1;
lpStr1 = buffer_1;

// String path name 2.
char buffer_2[MAX_PATH] = "C:\\path1\\path2\\sample.txt";
char *lpStr2;
lpStr2 = buffer_2;

// String path name 3.
char buffer_3[MAX_PATH] = "C:\\path1\\path2\\sample.txt";
char *lpStr3;
lpStr3 = buffer_3;

// String path name 4.
char buffer_4[MAX_PATH] = "C:\\path1\\path2\\sample.txt";
char *lpStr4;
lpStr4 = buffer_4;

// Variable to get the return from "PathCompactPath".
int retval;

cout << "The un-truncated path is                " << lpStr1 << endl;

retval = PathCompactPath(hdc,lpStr1,125);
cout << "The truncated path at 125 pixels is :   " << lpStr1 << endl;

retval = PathCompactPath(hdc,lpStr2,120);
cout << "The truncated path at 120 pixels is :   " << lpStr2 << endl;

retval = PathCompactPath(hdc,lpStr3,110);
cout << "The truncated path at 110 pixels is :   " << lpStr3 << endl;

retval = PathCompactPath(hdc,lpStr4,25);
cout << "The truncated path at  25 pixels is :   " << lpStr4 << endl;
}

OUTPUT:
===========
The un-truncated path is                C:\path1\path2\sample.txt
The truncated path at 125 pixels is :   C:\path1\...\sample.txt
The truncated path at 120 pixels is :   C:\pat...\sample.txt
The truncated path at 110 pixels is :   C:\p...\sample.txt
The truncated path at  25 pixels is :   ...\sample.txt
```





> [!NOTE]
> The shlwapi.h header defines PathCompactPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

