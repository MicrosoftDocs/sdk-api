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

# PathAddBackslashW function


## -description


Adds a backslash to the end of a string to create the correct syntax for a path. If the source path already has a trailing backslash, no backslash will be added.

            
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="https://msdn.microsoft.com/b50677cd-8815-4d84-b70a-c83863378c56">PathCchAddBackslash</a> or <a href="https://msdn.microsoft.com/89adf45f-f16d-49d1-9e76-b57b73b4d4c3">PathCchAddBackslashEx</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath

TBD




#### - lpszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a buffer with a string that represents a path. The size of this buffer must be set to MAX_PATH to ensure that it is large enough to hold the returned string.


## -returns



Type: <b>LPTSTR</b>

A pointer that, when this function returns successfully, points to the new string's terminating null character. If the backslash could not be appended due to inadequate buffer size, this value is <b>NULL</b>.



