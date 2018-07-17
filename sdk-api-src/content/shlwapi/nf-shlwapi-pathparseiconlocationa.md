---
UID: NF:shlwapi.PathParseIconLocationA
title: PathParseIconLocationA function
author: windows-sdk-content
description: Parses a file location string that contains a file location and icon index, and returns separate values.
old-location: shell\PathParseIconLocation.htm
old-project: shell
ms.assetid: 1ded2f0f-0e11-4730-ab7b-16536e7f4435
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: PathParseIconLocation, PathParseIconLocation function [Windows Shell], PathParseIconLocationA, PathParseIconLocationW, _win32_PathParseIconLocation, shell.PathParseIconLocation, shlwapi/PathParseIconLocation, shlwapi/PathParseIconLocationA, shlwapi/PathParseIconLocationW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathParseIconLocationW (Unicode) and PathParseIconLocationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
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
 - PathParseIconLocation
 - PathParseIconLocationA
 - PathParseIconLocationW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathParseIconLocationA function


## -description


Parses a file location string that contains a file location and icon index, and returns separate values.


## -parameters




### -param pszIconFile [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains a file location string. It should be in the form "<i>path</i>,<i>iconindex</i>". When the function returns, <i>pszIconFile</i> will point to the file's path.


## -returns



Type: <b>int</b>

Returns the valid icon index value.




## -remarks



This function is useful for taking a DefaultIcon value retrieved from the registry by <a href="https://msdn.microsoft.com/8cca6bfe-d365-4d10-bc8d-f3bebefaad02">SHGetValue</a> and separating the icon index from the path.


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

void main(void)
{
// Path to parse for file and icon index.
char buffer_1[ ] = "C:\\TEST\\sample.txt,3"; 
char *lpStr1;
lpStr1 = buffer_1;

// Return value from "PathParseIconLocation".
int retval;

// Search a path to parse for file and icon index.
retval = PathParseIconLocation(lpStr1);
cout &lt;&lt; "The path to parse for file and icon index is   : " &lt;&lt; lpStr1 &lt;&lt; endl;
cout &lt;&lt; "PathParseIconLocation returns the icon index of: " &lt;&lt; retval &lt;&lt; endl;
}

OUTPUT:
==========
The path to parse for file and icon index is   : C:\TEST\sample.txt
PathParseIconLocation returns the icon index of: 3</pre>
</td>
</tr>
</table></span></div>


