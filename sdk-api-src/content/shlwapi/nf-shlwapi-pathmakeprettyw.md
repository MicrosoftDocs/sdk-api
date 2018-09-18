---
UID: NF:shlwapi.PathMakePrettyW
title: PathMakePrettyW function
author: windows-sdk-content
description: Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.
old-location: shell\PathMakePretty.htm
tech.root: shell
ms.assetid: fb871054-4c63-42de-b85b-edefa4b09ea0
ms.author: windowssdkdev
ms.date: 09/14/2018
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

# PathMakePrettyW function


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



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;iostream.h&gt;
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
    cout &lt;&lt; "The content of the unconverted path is : " &lt;&lt; lpStr1 &lt;&lt; endl;
    cout &lt;&lt; "The \"PathMakePretty\" function returns the value " 
         &lt;&lt; PathMakePretty(lpStr1) &lt;&lt; "  = TRUE &amp; converts"  &lt;&lt; endl;
    cout &lt;&lt; "The content of the converted path is   : " &lt;&lt; lpStr1 &lt;&lt; endl;

// Test path name 2.
    cout &lt;&lt; "\nThe content of the unconverted path is : " &lt;&lt; lpStr2 &lt;&lt; endl;
    cout &lt;&lt; "The \"PathMakePretty\" function returns the value " 
         &lt;&lt; PathMakePretty(lpStr2) &lt;&lt; "  = FALSE &amp; no conversion"  &lt;&lt; endl;
    cout &lt;&lt; "The content of the converted path is   : " &lt;&lt; lpStr2 &lt;&lt; endl;
}

OUTPUT:
=============
The content of the unconverted path is : C:\TEST\FILE
The "PathMakePretty" function returns the value 1  = TRUE &amp; converts
The content of the converted path is   : C:\test\file

The content of the unconverted path is : c:\test\file
The "PathMakePretty" function returns the value 0  = FALSE &amp; no conversion
The content of the converted path is   : c:\test\file</pre>
</td>
</tr>
</table></span></div>


