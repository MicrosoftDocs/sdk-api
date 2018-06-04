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

# PathCchRenameExtension function


## -description



Replaces a file name's extension at the end of a path string with a new extension. If the path string does not end with an extension, the new extension is added.

This function differs from <a href="https://msdn.microsoft.com/3d94f67c-e3ee-4b64-b0b9-8f771423bdc5">PathRenameExtension</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function should be used in place of <a href="https://msdn.microsoft.com/3d94f67c-e3ee-4b64-b0b9-8f771423bdc5">PathRenameExtension</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, this value points to the same string, but with the renamed or added extension.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


### -param pszExt [in]

A pointer to the new extension string. The leading '.' character is optional. In the case of an empty string (""), any existing extension in the path string is removed.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



