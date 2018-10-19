---
UID: NF:shlwapi.PathFileExistsW
title: PathFileExistsW function
author: windows-sdk-content
description: Determines whether a path to a file system object such as a file or folder is valid.
old-location: shell\PathFileExists.htm
tech.root: shell
ms.assetid: 26d01e9f-cbf2-4e40-9970-a594879b424d
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: PathFileExists, PathFileExists function [Windows Shell], PathFileExistsA, PathFileExistsW, _win32_PathFileExists, shell.PathFileExists, shlwapi/PathFileExists, shlwapi/PathFileExistsA, shlwapi/PathFileExistsW
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
req.unicode-ansi: PathFileExistsW (Unicode) and PathFileExistsA (ANSI)
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
 - PathFileExists
 - PathFileExistsA
 - PathFileExistsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathFileExistsW function


## -description


Determines whether a path to a file system object such as a file or folder is valid.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the full path of the object to verify.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the file exists; otherwise, <b>FALSE</b>. Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for extended error information.




## -remarks



This function tests the validity of the path.

A path specified by Universal Naming Convention (UNC) is limited to a file only; that is, \\server\share\file is permitted. A UNC path to a server or server share is not permitted; that is, \\server or \\server\share. This function returns <b>FALSE</b> if a mounted remote drive is out of service.


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

void main(void)
{
    // Valid file path name (file is there).
    char buffer_1[ ] = "C:\\TEST\\file.txt"; 
    char *lpStr1;
    lpStr1 = buffer_1;
    
    // Invalid file path name (file is not there).
    char buffer_2[ ] = "C:\\TEST\\file.doc"; 
    char *lpStr2;
    lpStr2 = buffer_2;
    
    // Return value from "PathFileExists".
    int retval;
    
    // Search for the presence of a file with a true result.
    retval = PathFileExists(lpStr1);
    if(retval == 1)
    {
        cout &lt;&lt; "Search for the file path of : " &lt;&lt; lpStr1 &lt;&lt; endl;
        cout &lt;&lt; "The file requested \"" &lt;&lt; lpStr1 &lt;&lt; "\" is a valid file" &lt;&lt; endl;
        cout &lt;&lt; "The return from function is : " &lt;&lt; retval &lt;&lt; endl;
    }
    
    else
    {
        cout &lt;&lt; "\nThe file requested " &lt;&lt; lpStr1 &lt;&lt; " is not a valid file" &lt;&lt; endl;
        cout &lt;&lt; "The return from function is : " &lt;&lt; retval &lt;&lt; endl;
    }
    
    // Search for the presence of a file with a false result.
    retval = PathFileExists(lpStr2);
    
    if(retval == 1)
    {
        cout &lt;&lt; "\nThe file requested " &lt;&lt; lpStr2 &lt;&lt; "is a valid file" &lt;&lt; endl;
        cout &lt;&lt; "Search for the file path of : " &lt;&lt; lpStr2 &lt;&lt; endl;
        cout &lt;&lt; "The return from function is : " &lt;&lt; retval &lt;&lt; endl;
    }
    else
    {
        cout &lt;&lt; "\nThe file requested \"" &lt;&lt; lpStr2 &lt;&lt; "\" is not a valid file" &lt;&lt; endl;
        cout &lt;&lt; "The return from function is : " &lt;&lt; retval &lt;&lt; endl;
    }
}

OUTPUT
==============
Search for the file path of : C:\TEST\file.txt
The file requested "C:\TEST\file.txt" is a valid file
The return from function is : 1

The file requested "C:\TEST\file.doc" is not a valid file
The return from function is : 0</pre>
</td>
</tr>
</table></span></div>


