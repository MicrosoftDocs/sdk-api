---
UID: NF:shlwapi.PathGetArgsA
title: PathGetArgsA function
author: windows-sdk-content
description: Finds the command line arguments within a given path.
old-location: shell\PathGetArgs.htm
tech.root: shell
ms.assetid: 17dfb601-1306-41b6-a504-8bf69ff204c9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: PathGetArgs, PathGetArgs function [Windows Shell], PathGetArgsA, PathGetArgsW, _win32_PathGetArgs, shell.PathGetArgs, shlwapi/PathGetArgs, shlwapi/PathGetArgsA, shlwapi/PathGetArgsW
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
req.unicode-ansi: PathGetArgsW (Unicode) and PathGetArgsA (ANSI)
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
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathGetArgs
 - PathGetArgsA
 - PathGetArgsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathGetArgsA function


## -description


Finds the command line arguments within a given path.


## -parameters




### -param pszPath [in]

Type: <b>PTSTR</b>

Pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be searched.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to a null-terminated string that contains the arguments portion of the path if successful. 

                    

If there are no arguments in the path, the function returns a pointer to the end of the input string.

If the function is given a <b>NULL</b> argument it returns <b>NULL</b>.




## -remarks



This function should not be used on generic command path templates (from users or the registry), but rather should be used only on templates that the application knows to be well formed.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#include &lt;windows.h&gt;
#include &lt;iostream.h&gt;
#include "Shlwapi.h"

void main( void )
{
    // Path_1 to search for file arguments (2 arguments):
    char buffer_1[ ] = "test.exe temp.txt sample.doc"; 
    char *lpStr1;
    lpStr1 = buffer_1;
    
    // Path_2 to search for file arguments (3 arguments):
    char buffer_2[ ] = "test.exe 1 2 3"; 
    char *lpStr2;
    lpStr2 = buffer_2;
    
    // Path_3 to search for file arguments (3 arguments):
    char buffer_3[ ] = "test.exe sample All 15"; 
    char *lpStr3;
    lpStr3 = buffer_3;
    
    // Path_4 to search for file arguments (no arguments):
    char buffer_4[ ] = "test.exe"; 
    char *lpStr4;
    lpStr4 = buffer_4;
    
    cout &lt;&lt; "The path passed to the function was : " &lt;&lt; lpStr1 &lt;&lt;
            "\nThe arg(s)found in path 1 were      : " &lt;&lt; PathGetArgs(lpStr1) &lt;&lt; endl;
    
    cout &lt;&lt; "\nThe path passed to the function was : " &lt;&lt; lpStr2 &lt;&lt;
            "\nThe arg(s)found in path 2 were      : " &lt;&lt; PathGetArgs(lpStr2) &lt;&lt; endl;
    
    cout &lt;&lt; "\nThe path passed to the function was : " &lt;&lt; lpStr3 &lt;&lt;
            "\nThe arg(s)found in path 3 were      : " &lt;&lt; PathGetArgs(lpStr3) &lt;&lt; endl;
    
    cout &lt;&lt; "\nThe path passed to the function was : " &lt;&lt; lpStr4 &lt;&lt;
            "\nThe arg(s)found in path 4 were      : " &lt;&lt; PathGetArgs(lpStr4) &lt;&lt; endl;
}

OUTPUT:
===========
The path passed to the function was : test.exe temp.txt sample.doc
The arg(s)found in path 1 were      : temp.txt sample.doc

The path passed to the function was : test.exe 1 2 3
The arg(s)found in path 2 were      : 1 2 3

The path passed to the function was : test.exe sample All 15
The arg(s)found in path 3 were      : sample All 15

The path passed to the function was : test.exe
The arg(s)found in path 4 were      :
===========</pre>
</td>
</tr>
</table></span></div>


