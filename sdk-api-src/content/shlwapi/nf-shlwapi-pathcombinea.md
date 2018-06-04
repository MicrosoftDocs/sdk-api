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

# PathCombineA function


## -description


Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.
        
            
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="https://msdn.microsoft.com/506a4165-f572-4521-958f-56a0296f9c05">PathCchCombine</a> or <a href="https://msdn.microsoft.com/798c2e49-04a5-4270-b584-41faf1519e4b">PathCchCombineEx</a> function in its place.</div><div> </div>

## -parameters




### -param pszDest

TBD


### -param pszDir

TBD


### -param pszFile

TBD




#### - pszMore [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the second path. This value can be <b>NULL</b>.


#### - pszPathIn [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the first path. This value can be <b>NULL</b>.


#### - pszPathOut [out]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the combined path string. You must set the size of this buffer to MAX_PATH to ensure that it is large enough to hold the returned string.


## -returns



Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the concatenated path string. This is the same string pointed to by <i>pszPathOut</i>. If this function does not return successfully, this value is <b>NULL</b>.




## -remarks



The directory path should be in the form of A:,B:, ..., Z:. The file path should be in a correct form that represents the file name part of the path. If the directory path ends with a backslash, the backslash will be maintained. Note that while <i>lpszDir</i> and <i>lpszFile</i> are both optional parameters, they cannot both be <b>NULL</b>.


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
// Buffer to hold combined path.
char buffer_1[MAX_PATH] = "";
char *lpStr1;
lpStr1 = buffer_1;

// String for balance of path name.
char buffer_2[ ] = "One\\Two\\Three";
char *lpStr2;
lpStr2 = buffer_2;

// String for directory name.
char buffer_3[ ] = "C:";
char *lpStr3;
lpStr3 = buffer_3;

cout &lt;&lt; "The file path to be combined is  " 
     &lt;&lt; lpStr2 &lt;&lt; endl;
cout &lt;&lt; "The directory name path is       " 
     &lt;&lt; lpStr3 &lt;&lt; endl;
cout &lt;&lt; "The combined path is             " 
     &lt;&lt; PathCombine(lpStr1,lpStr3,lpStr2) &lt;&lt; endl;
}

------------
INPUT:
------------
Path for directory part: "C:"
Path for file part: "One\Two\Three"
------------
OUTPUT:
------------
The file path to be combined is  One\Two\Three
The directory name path is       C:
The combined path is             C:\One\Two\Three</pre>
</td>
</tr>
</table></span></div>


