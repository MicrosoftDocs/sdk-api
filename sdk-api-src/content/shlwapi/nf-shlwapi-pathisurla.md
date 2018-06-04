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
cout &lt;&lt; "The contents of String 1: " &lt;&lt; lpStr1
     &lt;&lt; "\nThe return value from the function is " &lt;&lt; retval &lt;&lt; " = TRUE" &lt;&lt; endl;

// Test path name 2.
retval = PathIsURL(lpStr2);
cout &lt;&lt; "The contents of String 2: " &lt;&lt; lpStr2
     &lt;&lt; "\nThe return value from the function is " &lt;&lt; retval &lt;&lt; " = TRUE" &lt;&lt; endl;

// Test path name 3.
retval = PathIsURL(lpStr3);
cout &lt;&lt; "The contents of String 3: " &lt;&lt; lpStr3
     &lt;&lt; "\nThe return value from the function is " &lt;&lt; retval &lt;&lt; " = FALSE"&lt;&lt; endl;
}

OUTPUT:
=============
The contents of String 1: http://www.microsoft.com/software/index.html
The return value from the function is 1 = TRUE
The contents of String 2: http://www.microsoft.com
The return value from the function is 1 = TRUE
The contents of String 3: microsoft.com
The return value from the function is 0 = FALSE</pre>
</td>
</tr>
</table></span></div>


