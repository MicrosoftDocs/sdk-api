---
UID: NF:shlwapi.PathIsURLA
title: PathIsURLA function
author: windows-sdk-content
description: Tests a given string to determine if it conforms to a valid URL format.
old-location: shell\PathIsURL.htm
tech.root: shell
ms.assetid: 8791bcd8-0d8f-4f7b-9c8e-59bcb95b5d19
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: PathIsURL, PathIsURL function [Windows Shell], PathIsURLA, PathIsURLW, _win32_PathIsURL, shell.PathIsURL, shlwapi/PathIsURL, shlwapi/PathIsURLA, shlwapi/PathIsURLW
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
req.unicode-ansi: PathIsURLW (Unicode) and PathIsURLA (ANSI)
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
 - API-MS-Win-Core-url-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathIsURL
 - PathIsURLA
 - PathIsURLW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathIsURLA function


## -description


Tests a given string to determine if it conforms to a valid URL format.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the URL path to validate.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>pszPath</i> has a valid URL format, or <b>FALSE</b> otherwise.




## -remarks



This function does not verify that the path points to an existing site—only that it has a valid URL format.


#### Examples




```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main( void )
{
// String path name 1.
char buffer_1[ ] = "http://www.microsoft.com/software/index.html";
char *lpStr1;
lpStr1 = buffer_1;

// String path name 2.
char buffer_2[ ] = "http://www.microsoft.com";
char *lpStr2;
lpStr2 = buffer_2;

// String path name 3.
char buffer_3[ ] = "microsoft.com";
char *lpStr3;
lpStr3 = buffer_3;

// Variable to get the return 
// from "PathIsURL".
int retval;

// Test path name 1.
retval = PathIsURL(lpStr1);
cout << "The contents of String 1: " << lpStr1
     << "\nThe return value from the function is " << retval << " = TRUE" << endl;

// Test path name 2.
retval = PathIsURL(lpStr2);
cout << "The contents of String 2: " << lpStr2
     << "\nThe return value from the function is " << retval << " = TRUE" << endl;

// Test path name 3.
retval = PathIsURL(lpStr3);
cout << "The contents of String 3: " << lpStr3
     << "\nThe return value from the function is " << retval << " = FALSE"<< endl;
}

OUTPUT:
=============
The contents of String 1: http://www.microsoft.com/software/index.html
The return value from the function is 1 = TRUE
The contents of String 2: http://www.microsoft.com
The return value from the function is 1 = TRUE
The contents of String 3: microsoft.com
The return value from the function is 0 = FALSE
```




