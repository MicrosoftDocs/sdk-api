---
UID: NF:shlwapi.PathFileExistsA
title: PathFileExistsA function (shlwapi.h)
description: Determines whether a path to a file system object such as a file or folder is valid. (ANSI)
helpviewer_keywords: ["PathFileExistsA", "shlwapi/PathFileExistsA"]
old-location: shell\PathFileExists.htm
tech.root: shell
ms.assetid: 26d01e9f-cbf2-4e40-9970-a594879b424d
ms.date: 12/05/2018
ms.keywords: PathFileExists, PathFileExists function [Windows Shell], PathFileExistsA, PathFileExistsW, _win32_PathFileExists, shell.PathFileExists, shlwapi/PathFileExists, shlwapi/PathFileExistsA, shlwapi/PathFileExistsW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathFileExistsW (Unicode) and PathFileExistsA (ANSI)
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
 - PathFileExistsA
 - shlwapi/PathFileExistsA
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
 - PathFileExists
 - PathFileExistsA
 - PathFileExistsW
---

# PathFileExistsA function


## -description

Determines whether a path to a file system object such as a file or folder is valid.

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the full path of the object to verify.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the file exists; otherwise, <b>FALSE</b>. Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

## -remarks

This function tests the validity of the path.

A path specified by Universal Naming Convention (UNC) is limited to a file only; that is, \\server\share\file is permitted. A UNC path to a server or server share is not permitted; that is, \\server or \\server\share. This function returns <b>FALSE</b> if a mounted remote drive is out of service.


#### Examples


```cpp

#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main(void)
{
    // Valid file path name (file is there).
    char buffer_1[ ] = "C:\\TEST\\file.txt"; 
    char *lpStr1;
    lpStr1 = buffer_1;
    
    // Invalid file path name (file is not there).
    char buffer_2[ ] = "C:\\TEST\\file.doc"; 
    char *lpStr2;
    lpStr2 = buffer_2;
    
    // Return value from "PathFileExists".
    int retval;
    
    // Search for the presence of a file with a true result.
    retval = PathFileExists(lpStr1);
    if(retval == 1)
    {
        cout << "Search for the file path of : " << lpStr1 << endl;
        cout << "The file requested \"" << lpStr1 << "\" is a valid file" << endl;
        cout << "The return from function is : " << retval << endl;
    }
    
    else
    {
        cout << "\nThe file requested " << lpStr1 << " is not a valid file" << endl;
        cout << "The return from function is : " << retval << endl;
    }
    
    // Search for the presence of a file with a false result.
    retval = PathFileExists(lpStr2);
    
    if(retval == 1)
    {
        cout << "\nThe file requested " << lpStr2 << "is a valid file" << endl;
        cout << "Search for the file path of : " << lpStr2 << endl;
        cout << "The return from function is : " << retval << endl;
    }
    else
    {
        cout << "\nThe file requested \"" << lpStr2 << "\" is not a valid file" << endl;
        cout << "The return from function is : " << retval << endl;
    }
}

OUTPUT
==============
Search for the file path of : C:\TEST\file.txt
The file requested "C:\TEST\file.txt" is a valid file
The return from function is : 1

The file requested "C:\TEST\file.doc" is not a valid file
The return from function is : 0
```





> [!NOTE]
> The shlwapi.h header defines PathFileExists as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
