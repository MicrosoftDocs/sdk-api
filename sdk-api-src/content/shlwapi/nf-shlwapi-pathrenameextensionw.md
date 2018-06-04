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

# PathRenameExtensionW function


## -description


Replaces the extension of a file name with a new extension. If the file name does not contain an extension, the extension will be attached to the end of the string.
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="https://msdn.microsoft.com/79cd9499-03b7-4482-abd3-a42edd1b2b67">PathCchRenameExtension</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

Pointer to a null-terminated string of length MAX_PATH in which to replace the extension.


### -param pszExt [in]

Type: <b>LPCTSTR</b>

Pointer to a character buffer that contains a '.' character followed by the new extension.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero if the new path and extension would exceed MAX_PATH characters.



