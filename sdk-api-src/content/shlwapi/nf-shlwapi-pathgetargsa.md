---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


