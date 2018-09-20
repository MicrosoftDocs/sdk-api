---
UID: NF:shlwapi.PathRemoveArgsA
title: PathRemoveArgsA function
author: windows-sdk-content
description: Removes any arguments from a given path.
old-location: shell\PathRemoveArgs.htm
tech.root: shell
ms.assetid: 430072bc-4ddc-4b3d-bf32-fb60d7b56faf
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: PathRemoveArgs, PathRemoveArgs function [Windows Shell], PathRemoveArgsA, PathRemoveArgsW, _win32_PathRemoveArgs, shell.PathRemoveArgs, shlwapi/PathRemoveArgs, shlwapi/PathRemoveArgsA, shlwapi/PathRemoveArgsW
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
req.unicode-ansi: PathRemoveArgsW (Unicode) and PathRemoveArgsA (ANSI)
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
 - PathRemoveArgs
 - PathRemoveArgsA
 - PathRemoveArgsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathRemoveArgsA function


## -description


Removes any arguments from a given path.


## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

Pointer to a null-terminated string of length MAX_PATH that contains the path from which to remove arguments.


## -returns



This function does not return a value.




## -remarks



This function should not be used on generic command path templates (from users or the registry), but rather it should be used only on templates that the application knows to be well formed.


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
    // Path with arguments.
    char buffer_1[ ] = "c:\\a\\b\\FileA Arg1 Arg2"; 
    char *lpStr1;
    lpStr1 = buffer_1;
    
    // Path before "PathRemoveArgs".
    cout &lt;&lt; "Path before calling \"PathRemoveArgs\": " &lt;&lt; lpStr1 &lt;&lt; endl;
    
    // Call function "PathRemoveArgs".
    PathRemoveArgs(lpStr1);
    
    // Path after "PathRemoveArgs".
    cout &lt;&lt; "Path after calling \"PathRemoveArgs\": " &lt;&lt; lpStr1 &lt;&lt; endl;
}

OUTPUT:
==================
Path before calling "PathRemoveArgs": c:\a\b\FileA Arg1 Arg2
Path after calling "PathRemoveArgs": c:\a\b\FileA</pre>
</td>
</tr>
</table></span></div>


