---
UID: NF:shlwapi.PathRelativePathToA
title: PathRelativePathToA function (shlwapi.h)
description: Creates a relative path from one file or folder to another. (ANSI)
helpviewer_keywords: ["PathRelativePathToA", "shlwapi/PathRelativePathToA"]
old-location: shell\PathRelativePathTo.htm
tech.root: shell
ms.assetid: 7ed8d50a-2ad4-4ddf-941d-aea593341592
ms.date: 12/05/2018
ms.keywords: PathRelativePathTo, PathRelativePathTo function [Windows Shell], PathRelativePathToA, PathRelativePathToW, _win32_PathRelativePathTo, shell.PathRelativePathTo, shlwapi/PathRelativePathTo, shlwapi/PathRelativePathToA, shlwapi/PathRelativePathToW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathRelativePathToW (Unicode) and PathRelativePathToA (ANSI)
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
 - PathRelativePathToA
 - shlwapi/PathRelativePathToA
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
 - PathRelativePathTo
 - PathRelativePathToA
 - PathRelativePathToW
---

# PathRelativePathToA function


## -description

Creates a relative path from one file or folder to another.

## -parameters

### -param pszPath [out]

Type: <b>LPTSTR</b>

A pointer to a string that receives the relative path. This buffer must be at least MAX_PATH characters in size.

### -param pszFrom [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path that defines the start of the relative path.

### -param dwAttrFrom [in]

Type: <b>DWORD</b>

The file attributes of <i>pszFrom</i>. If this value contains FILE_ATTRIBUTE_DIRECTORY, <i>pszFrom</i> is assumed to be a directory; otherwise, <i>pszFrom</i> is assumed to be a file.

### -param pszTo [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path that defines the endpoint of the relative path.

### -param dwAttrTo [in]

Type: <b>DWORD</b>

The file attributes of <i>pszTo</i>. If this value contains FILE_ATTRIBUTE_DIRECTORY, <i>pszTo</i> is assumed to be directory; otherwise, <i>pszTo</i> is assumed to be a file.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

This function takes a pair of paths and generates a relative path from one to the other. The paths do not have to be fully qualified, but they must have a common prefix, or the function will fail and return <b>FALSE</b>.

For example, let the starting point, <i>pszFrom</i>, be "c:\FolderA\FolderB\FolderC", and the ending point, <i>pszTo</i>, be "c:\FolderA\FolderD\FolderE". <b>PathRelativePathTo</b> will return the relative path from <i>pszFrom</i> to <i>pszTo</i> as: "..\..\FolderD\FolderE". You will get the same result if you set <i>pszFrom</i> to "\FolderA\FolderB\FolderC" and <i>pszTo</i> to "\FolderA\FolderD\FolderE". On the other hand, "c:\FolderA\FolderB" and "a:\FolderA\FolderD do not share a common prefix, and the function will fail. Note that "\\" is not considered a prefix and is ignored. If you set <i>pszFrom</i> to "\\FolderA\FolderB", and <i>pszTo</i> to "\\FolderC\FolderD", the function will fail.


#### Examples




```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main(void)
{
    char szOut[MAX_PATH] = "";
    char szFrom[ ] = "c:\\a\\b\\path";
    char szTo[ ] = "c:\\a\\x\\y\\file";

    cout  <<  "The relative path is relative from: ";
    cout  <<  szFrom;
    cout  <<  "\n";

    cout  <<  "The relative path is relative to: ";
    cout  <<  szTo;
    cout  <<  "\n";

    PathRelativePathTo(szOut,
                       szFrom,
                       FILE_ATTRIBUTE_DIRECTORY,
                       szTo,
                       FILE_ATTRIBUTE_NORMAL);

    cout  <<  "The relative path is: ";
    cout  <<  szOut;
    cout  <<  "\n";
}

OUTPUT:
==================
The relative path is relative from: c:\a\b\path
The relative path is relative to: c:\a\x\y\file
The relative path is: ..\..\x\y\file
```





> [!NOTE]
> The shlwapi.h header defines PathRelativePathTo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

