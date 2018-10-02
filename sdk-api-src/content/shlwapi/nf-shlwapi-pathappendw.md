---
UID: NF:shlwapi.PathAppendW
title: PathAppendW function
author: windows-sdk-content
description: Appends one path to the end of another.
old-location: shell\PathAppend.htm
tech.root: Shell
ms.assetid: 896737ef-a05c-4f0f-b8b0-56355ae9c2d9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: PathAppend, PathAppend function [Windows Shell], PathAppendA, PathAppendW, _win32_PathAppend, shell.PathAppend, shlwapi/PathAppend, shlwapi/PathAppendA, shlwapi/PathAppendW
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
req.unicode-ansi: PathAppendW (Unicode) and PathAppendA (ANSI)
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
 - PathAppend
 - PathAppendA
 - PathAppendW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathAppendW function


## -description


Appends one path to the end of another.
        
            
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="https://msdn.microsoft.com/b64884ad-15c7-495e-8037-34daf68f8cf7">PathCchAppend</a> or <a href="https://msdn.microsoft.com/5421c666-1c8a-4ae8-baba-9e6f69c877df">PathCchAppendEx</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string to which the path specified in <i>pszMore</i> is appended. You must set the size of this buffer to MAX_PATH to ensure that it is large enough to hold the returned string.


### -param pszMore [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be appended.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



This function automatically inserts a backslash between the two strings, if one is not already present.

The path supplied in <i>pszPath</i> cannot begin with "..\\" or ".\\" to produce a relative path string. If present, those periods are stripped from the output string. For example, appending "path3" to "..\\path1\\path2" results in an output of "\path1\path2\path3" rather than "..\path1\path2\path3".


#### Examples



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#include &lt;windows.h&gt;
#include &lt;iostream&gt;
#include "Shlwapi.h"

using namespace std;

int main( void )
{
	// String for path name.
	char buffer_1[MAX_PATH] = "name_1\\name_2";
	char *lpStr1;
	lpStr1 = buffer_1;

	// String of what is being added.
	char buffer_2[ ] = "name_3";
	char *lpStr2;
	lpStr2 = buffer_2;

	cout &lt;&lt; "The original path string is    " &lt;&lt; lpStr1 &lt;&lt; endl;
	cout &lt;&lt; "The part to append to end is   " &lt;&lt; lpStr2 &lt;&lt; endl;
	bool ret = PathAppend(lpStr1,lpStr2);
	cout &lt;&lt; "The appended path string is    " &lt;&lt; lpStr1 &lt;&lt; endl;
}

OUTPUT:
--------- 
The original path string is    name_1\name_2
The part to append to end is   name_3
The appended path string is    name_1\name_2\name_3</pre>
</td>
</tr>
</table></span></div>


