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

# PathAddExtensionW function


## -description


Adds a file name extension to a path string.
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="https://msdn.microsoft.com/c37b438b-39e7-4f24-b076-2401900dab71">PathCchAddExtension</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a buffer with the null-terminated string to which the file name extension will be appended. You must set the size of this buffer to MAX_PATH to ensure that it is large enough to hold the returned string.


### -param pszExt

TBD




#### - pszExtension [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the file name extension. This value can be <b>NULL</b>.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if an extension was added, or <b>FALSE</b> otherwise.




## -remarks



If there is already a file name extension present, no extension will be added. If the <i>pszPath</i> points to a <b>NULL</b> string, the result will be the file name extension only. If <i>pszExtension</i> points to a <b>NULL</b> string, an ".exe" extension will be added.


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
     // String for path name without file name extension.
     char buffer_1[MAX_PATH] = "file";
     char *lpStr1;
     lpStr1 = buffer_1;

     // String for path name with file name extension.
     char buffer_2[ ] = "file.doc";
     char *lpStr2;
     lpStr2 = buffer_2;

     // String for extension name.
     char F_Ext[MAX_PATH] = ".txt";
     char *lpStr3;
     lpStr3 = F_Ext;

     // Null string as path. 
     char N_String[MAX_PATH] = "\0";
     char *lpStr4;
     lpStr4 = N_String;

     // Path 1 without the file name extension.
     cout &lt;&lt; "The original path string 1 is  " &lt;&lt; lpStr1 &lt;&lt; endl;

     int ret_1 = PathAddExtension(lpStr1,lpStr3);
     cout &lt;&lt; "The modified path string 1 is  " &lt;&lt; lpStr1 &lt;&lt; endl;

    // Path 2 with the file name extension already there.
    cout &lt;&lt; "The original path string 2 is  " &lt;&lt; lpStr2 &lt;&lt; endl;
    int ret_2 = PathAddExtension(lpStr2,lpStr3);
    cout &lt;&lt; "The modified path string 2 is  " &lt;&lt; lpStr2&lt;&lt; endl;

    // Path 3 null string as a path.
    int ret_3 = PathAddExtension(lpStr4,lpStr3);
    cout &lt;&lt; "The return value is " &lt;&lt; ret_3&lt;&lt; endl;
    cout &lt;&lt; "The modified path on a null string is " &lt;&lt; lpStr4&lt;&lt; endl;

}

OUTPUT:
-----------------------
The original path string 1 is  file
The modified path string 1 is  file.txt
The original path string 2 is  file.doc
The modified path string 2 is  file.doc
The return value is 1
The modified path on a null string is .txt
The return value is 1</pre>
</td>
</tr>
</table></span></div>


