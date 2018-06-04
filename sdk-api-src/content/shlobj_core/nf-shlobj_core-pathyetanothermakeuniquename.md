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

# PathYetAnotherMakeUniqueName function


## -description


Creates a unique filename based on an existing filename.


## -parameters




### -param pszUniqueName [out]

Type: <b>PWSTR</b>

A string buffer that receives a null-terminated Unicode string that contains the fully qualified path of the unique file name. This buffer should be at least MAX_PATH characters long to avoid causing a buffer overrun.


### -param pszPath [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the fully qualified path of folder that will contain the new file. If <i>pszShort</i> is set to <b>NULL</b>, this string must contain a full destination path, ending with the long file name that the new file name will be base on.


### -param pszShort [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the short file name that the unique name will be based on. Set this value to <b>NULL</b> to create a name based on the long file name.


### -param pszFileSpec [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the long file name that the unique name will be based on.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if a unique name was successfully created; otherwise <b>FALSE</b>.




## -remarks



If the generated path exceeds MAX_PATH characters, this function may return a truncated string in <b>PathYetAnotherMakeUniqueName</b>. In that case, the function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/8456ae0c-e83c-43d0-a86a-1861a373d237">PathMakeUniqueName</a>
 

 

