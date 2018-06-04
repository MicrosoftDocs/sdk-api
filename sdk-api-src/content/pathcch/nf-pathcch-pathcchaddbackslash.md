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

# PathCchAddBackslash function


## -description



Adds a backslash to the end of a string to create the correct syntax for a path. If the source path already has a trailing backslash, no backslash will be added.

This function differs from <b>PathCchAddBackslash</b> in that you are restricted to a final path of length MAX_PATH.

This function differs from <a href="https://msdn.microsoft.com/27d8aec7-8b00-412a-9a42-8ce27e262781">PathAddBackslash</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function, or <a href="https://msdn.microsoft.com/89adf45f-f16d-49d1-9e76-b57b73b4d4c3">PathCchAddBackslashEx</a>, should be used in place of <a href="https://msdn.microsoft.com/27d8aec7-8b00-412a-9a42-8ce27e262781">PathAddBackslash</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the buffer contains the string with the appended backslash. This value should not be <b>NULL</b>.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


## -returns



This function returns S_OK if the function was successful, S_FALSE if the path string already ends in a backslash, or an error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/89adf45f-f16d-49d1-9e76-b57b73b4d4c3">PathCchAddBackslashEx</a>
 

 

