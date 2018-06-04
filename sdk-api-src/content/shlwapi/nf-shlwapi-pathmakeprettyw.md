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

# PathMakePrettyW function


## -description


Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.


## -parameters




### -param pszPath

TBD




#### - lpPath [in, out]

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


