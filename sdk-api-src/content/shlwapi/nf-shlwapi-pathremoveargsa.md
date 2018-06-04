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


