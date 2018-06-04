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

# PathIsRootW function


## -description


Determines whether a path string refers to the root of a volume.


## -parameters




### -param pszPath

TBD




#### - pPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be validated.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the specified path is a root, or <b>FALSE</b> otherwise.




## -remarks



Returns <b>TRUE</b> for paths such as "\", "<i>X</i>:\" or "\\<i>server</i>\<i>share</i>". Paths such as "..\path2" or "\\<i>server</i>\" return <b>FALSE</b>.
            


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
char buffer_1[ ] = "C:\\";
char *lpStr1;
lpStr1 = buffer_1;

// String path name 2.
char buffer_2[ ] = "path\\file";
char *lpStr2;
lpStr2 = buffer_2;

// Variable to get the return from "PathIsRoot".
int retval;

// Test case with path not absolute.
retval = PathIsRoot(lpStr1);
cout &lt;&lt; "The return from function is       :" &lt;&lt; retval &lt;&lt; endl;
cout &lt;&lt; "The path does contain a root part :" &lt;&lt; lpStr1 &lt;&lt; endl;

// Test case with path absolute.
retval = PathIsRoot(lpStr2);
cout &lt;&lt; "The return from function is       :" &lt;&lt; retval &lt;&lt; endl;
cout &lt;&lt; "The path does not contain part    :" &lt;&lt; lpStr2 &lt;&lt; endl;
}

OUTPUT:
============
The return from function is       :1
The path does contain a root part :C:\
The return from function is       :0
The path does not contain part    :path\file
============</pre>
</td>
</tr>
</table></span></div>


