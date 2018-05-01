---
UID: NF:shlwapi.PathCompactPathW
title: PathCompactPathW function
author: windows-driver-content
description: Truncates a file path to fit within a given pixel width by replacing path components with ellipses.
old-location: shell\PathCompactPath.htm
old-project: shell
ms.assetid: b8184c98-1f86-4714-baf8-af4ef3e71cf2
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: PathCompactPath, PathCompactPath function [Windows Shell], PathCompactPathA, PathCompactPathW, _win32_PathCompactPath, shell.PathCompactPath, shlwapi/PathCompactPath, shlwapi/PathCompactPathA, shlwapi/PathCompactPathW
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
req.unicode-ansi: PathCompactPathW (Unicode) and PathCompactPathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
-	api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
-	PathCompactPath
-	PathCompactPathA
-	PathCompactPathW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathCompactPathW function


## -description


Truncates a file path to fit within a given pixel width by replacing path components with ellipses.


## -parameters




### -param hDC [in]

Type: <b>HDC</b>

A handle to the device context used for font metrics. This value can be <b>NULL</b>.


### -param pszPath

TBD


### -param dx [in]

Type: <b>UINT</b>

The width, in pixels, in which the string must fit.


#### - lpszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be modified. On return, this buffer will contain the modified string.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the path was successfully compacted to the specified width. Returns <b>FALSE</b> on failure, or if the base portion of the path would not fit the specified width.




## -remarks



This function uses the font currently selected in <i>hDC</i> to calculate the width of the text. This function will not compact the path beyond the base file name preceded by ellipses.


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

HDC hdc;  /* display DC handle to current font metrics */ 

void main( void )
{
// String path name 1.
char buffer_1[MAX_PATH] = "C:\\path1\\path2\\sample.txt";
char *lpStr1;
lpStr1 = buffer_1;

// String path name 2.
char buffer_2[MAX_PATH] = "C:\\path1\\path2\\sample.txt";
char *lpStr2;
lpStr2 = buffer_2;

// String path name 3.
char buffer_3[MAX_PATH] = "C:\\path1\\path2\\sample.txt";
char *lpStr3;
lpStr3 = buffer_3;

// String path name 4.
char buffer_4[MAX_PATH] = "C:\\path1\\path2\\sample.txt";
char *lpStr4;
lpStr4 = buffer_4;

// Variable to get the return from "PathCompactPath".
int retval;

cout &lt;&lt; "The un-truncated path is                " &lt;&lt; lpStr1 &lt;&lt; endl;

retval = PathCompactPath(hdc,lpStr1,125);
cout &lt;&lt; "The truncated path at 125 pixels is :   " &lt;&lt; lpStr1 &lt;&lt; endl;

retval = PathCompactPath(hdc,lpStr2,120);
cout &lt;&lt; "The truncated path at 120 pixels is :   " &lt;&lt; lpStr2 &lt;&lt; endl;

retval = PathCompactPath(hdc,lpStr3,110);
cout &lt;&lt; "The truncated path at 110 pixels is :   " &lt;&lt; lpStr3 &lt;&lt; endl;

retval = PathCompactPath(hdc,lpStr4,25);
cout &lt;&lt; "The truncated path at  25 pixels is :   " &lt;&lt; lpStr4 &lt;&lt; endl;
}

OUTPUT:
===========
The un-truncated path is                C:\path1\path2\sample.txt
The truncated path at 125 pixels is :   C:\path1\...\sample.txt
The truncated path at 120 pixels is :   C:\pat...\sample.txt
The truncated path at 110 pixels is :   C:\p...\sample.txt
The truncated path at  25 pixels is :   ...\sample.txt</pre>
</td>
</tr>
</table></span></div>


