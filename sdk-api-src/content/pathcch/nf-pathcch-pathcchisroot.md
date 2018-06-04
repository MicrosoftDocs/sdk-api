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

# PathCchIsRoot function


## -description



Determines whether a path string refers to the root of a volume.

This function differs from <a href="https://msdn.microsoft.com/8586df98-91c4-49a6-9b07-7dceb8a63431">PathIsRoot</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.




## -parameters




### -param pszPath [in, optional]

A pointer to the path string.


## -returns



Returns <b>TRUE</b> if the specified path is a root, or <b>FALSE</b> otherwise.




## -remarks



The following table shows the <b>PathCchIsRoot</b> return value for various paths.
            
                

<table class="clsStd">
<tr>
<th>Path</th>
<th>PathCchIsRoot</th>
</tr>
<tr>
<td>"c:\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"c:"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"c:\path1"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\path1"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"path1"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\path1\path2"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\path1\path2\"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\path1\path2\path3"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\path1"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\path1\"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\UNC\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\UNC\path1\path2"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\UNC\path1\path2\"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\UNC\path1\path2\path3"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\UNC\path1"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\UNC\path1\"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\c:\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\c:"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\c:\path1"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\Volume{guid}\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\Volume{guid}"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\Volume{guid}\path1"</td>
<td>FALSE</td>
</tr>
<tr>
<td>NULL</td>
<td>FALSE</td>
</tr>
<tr>
<td>""</td>
<td>FALSE</td>
</tr>
</table>
 

This function returns <b>TRUE</b> for paths such as "\", "<i>X</i>:\" or "\\<i>server</i>\<i>share</i>". Paths such as "..\path2" or "\\<i>server</i>\" return <b>FALSE</b>.
            



