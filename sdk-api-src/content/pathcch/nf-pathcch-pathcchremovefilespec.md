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

# PathCchRemoveFileSpec function


## -description



Removes the last element in a path string, whether that element is a file name or a directory name. The element's leading backslash is also removed.

This function differs from <a href="https://msdn.microsoft.com/c47bcf8a-c59d-4d6a-81a9-a3960ae39867">PathRemoveFileSpec</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function should be used in place of <a href="https://msdn.microsoft.com/c47bcf8a-c59d-4d6a-81a9-a3960ae39867">PathRemoveFileSpec</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the fully-qualified path string. When this function returns successfully, the string will have had its last element and its leading backslash removed. This function does not affect root paths such as "C:\". In the case of a root path, the path string is returned unaltered. If a path string ends with a trailing backslash, only that backslash is removed.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


## -returns



This function returns S_OK if the function was successful, S_FALSE if there was nothing to remove, or an error code otherwise.




## -remarks



The following table shows the effect of this function on a selection of path strings.
            
                

<table class="clsStd">
<tr>
<th>Original String</th>
<th>Returned String</th>
</tr>
<tr>
<td>"C:\path1"</td>
<td>"C:\"</td>
</tr>
<tr>
<td>"C:\path1\path2"</td>
<td>"C:\path1"</td>
</tr>
<tr>
<td>"C:\path1\"</td>
<td>"C:\path1"</td>
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
 



