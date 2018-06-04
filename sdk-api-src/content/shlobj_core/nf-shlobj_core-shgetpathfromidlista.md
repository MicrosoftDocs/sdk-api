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

# SHGetPathFromIDListA function


## -description


Converts an item identifier list to a file system path.


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The address of an item identifier list that specifies a file or directory location relative to the root of the namespace (the desktop).


### -param pszPath [out]

Type: <b>LPTSTR</b>

The address of a buffer to receive the file system path. This buffer must be at least MAX_PATH characters in size.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.




## -remarks



If the location specified by the <i>pidl</i> parameter is not part of the file system, this function will fail.

If the <i>pidl</i> parameter specifies a shortcut, the <i>pszPath</i> will contain the path to the shortcut, not to the shortcut's target.




## -see-also




<a href="https://msdn.microsoft.com/80270c59-275d-4b13-b16c-0c07bb79ed8e">SHGetPathFromIDListEx</a>



<a href="https://msdn.microsoft.com/7bdfeed5-dcd0-40f6-a9d0-08ce816ee055">SHParseDisplayName</a>
 

 

