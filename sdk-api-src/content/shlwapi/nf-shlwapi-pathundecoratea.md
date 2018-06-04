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


