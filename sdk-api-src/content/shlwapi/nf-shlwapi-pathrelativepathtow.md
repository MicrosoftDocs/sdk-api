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

# PathRelativePathToW function


## -description


Creates a relative path from one file or folder to another.


## -parameters




### -param pszPath [out]

Type: <b>LPTSTR</b>

A pointer to a string that receives the relative path. This buffer must be at least MAX_PATH characters in size.


### -param pszFrom [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path that defines the start of the relative path.


### -param dwAttrFrom [in]

Type: <b>DWORD</b>

The file attributes of <i>pszFrom</i>. If this value contains FILE_ATTRIBUTE_DIRECTORY, <i>pszFrom</i> is assumed to be a directory; otherwise, <i>pszFrom</i> is assumed to be a file.


### -param pszTo [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path that defines the endpoint of the relative path.


### -param dwAttrTo [in]

Type: <b>DWORD</b>

The file attributes of <i>pszTo</i>. If this value contains FILE_ATTRIBUTE_DIRECTORY, <i>pszTo</i> is assumed to be directory; otherwise, <i>pszTo</i> is assumed to be a file.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



This function takes a pair of paths and generates a relative path from one to the other. The paths do not have to be fully qualified, but they must have a common prefix, or the function will fail and return <b>FALSE</b>.

For example, let the starting point, <i>pszFrom</i>, be "c:\FolderA\FolderB\FolderC", and the ending point, <i>pszTo</i>, be "c:\FolderA\FolderD\FolderE". <b>PathRelativePathTo</b> will return the relative path from <i>pszFrom</i> to <i>pszTo</i> as: "..\..\FolderD\FolderE". You will get the same result if you set <i>pszFrom</i> to "\FolderA\FolderB\FolderC" and <i>pszTo</i> to "\FolderA\FolderD\FolderE". On the other hand, "c:\FolderA\FolderB" and "a:\FolderA\FolderD do not share a common prefix, and the function will fail. Note that "\\" is not considered a prefix and is ignored. If you set <i>pszFrom</i> to "\\FolderA\FolderB", and <i>pszTo</i> to "\\FolderC\FolderD", the function will fail.


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
    char szOut[MAX_PATH] = "";
    char szFrom[ ] = "c:\\a\\b\\path";
    char szTo[ ] = "c:\\a\\x\\y\\file";

    cout  &lt;&lt;  "The relative path is relative from: ";
    cout  &lt;&lt;  szFrom;
    cout  &lt;&lt;  "\n";

    cout  &lt;&lt;  "The relative path is relative to: ";
    cout  &lt;&lt;  szTo;
    cout  &lt;&lt;  "\n";

    PathRelativePathTo(szOut,
                       szFrom,
                       FILE_ATTRIBUTE_DIRECTORY,
                       szTo,
                       FILE_ATTRIBUTE_NORMAL);

    cout  &lt;&lt;  "The relative path is: ";
    cout  &lt;&lt;  szOut;
    cout  &lt;&lt;  "\n";
}

OUTPUT:
==================
The relative path is relative from: c:\a\b\path
The relative path is relative to: c:\a\x\y\file
The relative path is: ..\..\x\y\file</pre>
</td>
</tr>
</table></span></div>


