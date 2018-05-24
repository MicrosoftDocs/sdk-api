---
UID: NF:shlwapi.PathUndecorateA
title: PathUndecorateA function
author: windows-driver-content
description: Removes the decoration from a path string.
old-location: shell\PathUndecorate.htm
old-project: shell
ms.assetid: 2d98ad60-8a7d-4b8d-9b5c-27e348bdc2c3
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: PathUndecorate, PathUndecorate function [Windows Shell], PathUndecorateA, PathUndecorateW, _win32_PathUndecorate, shell.PathUndecorate, shlwapi/PathUndecorate, shlwapi/PathUndecorateA, shlwapi/PathUndecorateW
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
req.unicode-ansi: PathUndecorateW (Unicode) and PathUndecorateA (ANSI)
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
-	API-MS-Win-shlwapi-IE-l1-1-0.dll
api_name:
-	PathUndecorate
-	PathUndecorateA
-	PathUndecorateW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathUndecorateA function


## -description


Removes the decoration from a path string.


## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A null-terminated string of length MAX_PATH that contains the path. When the function returns, <i>pszPath</i> points to the undecorated string.


## -returns



This function does not return a value.




## -remarks



A decoration consists of a pair of square brackets with one or more digits in between, inserted immediately after the base name and before the file name extension.


#### Examples

The following table illustrates how strings are modified by <b>PathUndecorate</b>.
					

<table class="clsStd">
<tr>
<th>Initial String</th>
<th>Undecorated String</th>
</tr>
<tr>
<td>C:\Path\File[5].txt</td>
<td>C:\Path\File.txt</td>
</tr>
<tr>
<td>C:\Path\File[12]</td>
<td>C:\Path\File</td>
</tr>
<tr>
<td>C:\Path\File.txt</td>
<td>C:\Path\File.txt</td>
</tr>
<tr>
<td>C:\Path\[3].txt</td>
<td>C:\Path\[3].txt</td>
</tr>
</table>
 

<div class="code"></div>


