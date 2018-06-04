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

# PathCchStripToRoot function


## -description



Removes all file and directory elements in a path except for the root information.

This function differs from <a href="https://msdn.microsoft.com/ce9a1a40-2a03-44d2-80bc-0dc10654550b">PathStripToRoot</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function should be used in place of <a href="https://msdn.microsoft.com/ce9a1a40-2a03-44d2-80bc-0dc10654550b">PathStripToRoot</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, this string contains only the root information taken from that path.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


## -returns



This function returns S_OK if the path was truncated, S_FALSE if the path was already just a root, or an HRESULT failure code.




## -remarks



Some examples of the effect of this function:
            
                

<table class="clsStd">
<tr>
<th>Initial string</th>
<th>Final string</th>
</tr>
<tr>
<td>"C:\path1\path2\file"</td>
<td>"C:\"</td>
</tr>
<tr>
<td>"\\path1\path2\path3"</td>
<td>"\\path1\path2"</td>
</tr>
<tr>
<td>"\path1"</td>
<td>"\"</td>
</tr>
</table>
 



