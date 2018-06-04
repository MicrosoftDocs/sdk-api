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

# PathStripToRootW function


## -description


Removes all file and directory elements in a path except for the root information.
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="https://msdn.microsoft.com/e0539478-8c64-4445-ab99-22f1df70afe8">PathCchStripToRoot</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath

TBD




#### - szRoot [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be converted. When this function returns successfully, this string contains only the root information taken from that path.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if a valid drive letter was found in the path, or <b>FALSE</b> otherwise.



