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

# PathParseIconLocationW function


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


