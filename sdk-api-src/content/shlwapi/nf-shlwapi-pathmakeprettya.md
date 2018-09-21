---
UID: NF:shlwapi.PathMakePrettyA
title: PathMakePrettyA function
author: windows-sdk-content
description: Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.
old-location: shell\PathMakePretty.htm
tech.root: shell
ms.assetid: fb871054-4c63-42de-b85b-edefa4b09ea0
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: PathMakePretty, PathMakePretty function [Windows Shell], PathMakePrettyA, PathMakePrettyW, _win32_PathMakePretty, shell.PathMakePretty, shlwapi/PathMakePretty, shlwapi/PathMakePrettyA, shlwapi/PathMakePrettyW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathMakePrettyW (Unicode) and PathMakePrettyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
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
 - PathMakePretty
 - PathMakePrettyA
 - PathMakePrettyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathMakePrettyA function


## -description


Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.


## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be converted.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the path has been converted, or <b>FALSE</b> otherwise.




## -remarks



This function only operates on paths that are entirely uppercase. For example: C:\WINDOWS will be converted to c:\windows, but c:\Windows will not be changed.


#### Examples




```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main( void )
{
// Path name 1.
char buffer_1[ ] = "C:\\TEST\\FILE";
char *lpStr1;
lpStr1 = buffer_1;

// Path name 2.
char buffer_2[ ] = "c:\\test\\file";
char *lpStr2;
lpStr2 = buffer_2;

// Test path name 1.
    cout << "The content of the unconverted path is : " << lpStr1 << endl;
    cout << "The \"PathMakePretty\" function returns the value " 
         << PathMakePretty(lpStr1) << "  = TRUE & converts"  << endl;
    cout << "The content of the converted path is   : " << lpStr1 << endl;

// Test path name 2.
    cout << "\nThe content of the unconverted path is : " << lpStr2 << endl;
    cout << "The \"PathMakePretty\" function returns the value " 
         << PathMakePretty(lpStr2) << "  = FALSE & no conversion"  << endl;
    cout << "The content of the converted path is   : " << lpStr2 << endl;
}

OUTPUT:
=============
The content of the unconverted path is : C:\TEST\FILE
The "PathMakePretty" function returns the value 1  = TRUE & converts
The content of the converted path is   : C:\test\file

The content of the unconverted path is : c:\test\file
The "PathMakePretty" function returns the value 0  = FALSE & no conversion
The content of the converted path is   : c:\test\file
```




