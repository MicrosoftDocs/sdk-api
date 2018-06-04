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

# PathRemoveBackslashA function


## -description


Removes the trailing backslash from a given path.
<div class="alert"><b>Note</b>  This function is deprecated. We recommend the use of the <a href="https://msdn.microsoft.com/61afc20e-ee6c-46ad-a058-64c57de41ba4">PathCchRemoveBackslash</a> or <a href="https://msdn.microsoft.com/250c2faa-94bb-42c1-97d4-37f8f59dbde6">PathCchRemoveBackslashEx</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath

TBD




#### - lpszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path from which to remove the backslash.


## -returns



Type: <b>LPTSTR</b>

A pointer that, when this function returns successfully and if a backslash has been removed, points to the terminating null character that has replaced the backslash at the end of the string. If the path did not include a trailing backslash, this value will point to the final character in the string.



