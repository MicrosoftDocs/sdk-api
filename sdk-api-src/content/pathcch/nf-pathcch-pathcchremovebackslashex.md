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

# PathCchRemoveBackslashEx function


## -description



Removes the trailing backslash from the end of a path string.

This function differs from <a href="https://msdn.microsoft.com/61afc20e-ee6c-46ad-a058-64c57de41ba4">PathCchRemoveBackslash</a> in that it can return a pointer to the new end of the string and report the number of unused characters remaining in the buffer.

This function differs from <a href="https://msdn.microsoft.com/58d13c38-40aa-4aaa-81dc-2b68425f1fe0">PathRemoveBackslash</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function, or <a href="https://msdn.microsoft.com/61afc20e-ee6c-46ad-a058-64c57de41ba4">PathCchRemoveBackslash</a>, should be used in place of <a href="https://msdn.microsoft.com/58d13c38-40aa-4aaa-81dc-2b68425f1fe0">PathRemoveBackslash</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the string contains the path with any trailing backslash removed. If no trailing backslash was found, the string is unchanged.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


### -param ppszEnd [out, optional]

A value that, when this function returns successfully, receives the address of a pointer to end of the new string. If the string is a root path such as "C:\", the pointer points to the backslash; otherwise the pointer points to the string's terminating null character.


### -param pcchRemaining [out, optional]

A pointer to a value that, when this function returns successfully, receives the number of unused characters in the destination buffer, including the terminating null character. If the string is a root path such as "C:\", this count includes the backslash in that string.


## -returns



This function returns S_OK if the function was successful, S_FALSE if the string was a root path or if no backslash was found, or an error code otherwise.




## -remarks



This function will not remove the backslash from a root path string, such as "C:\".



