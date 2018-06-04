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

# PathBuildRootW function


## -description


Creates a root path from a given drive number.


## -parameters




### -param pszRoot

TBD


### -param iDrive [in]

Type: <b>int</b>

A variable of type <b>int</b> that indicates the desired drive number. It should be between 0 and 25.


#### - szRoot [out]

Type: <b>LPTSTR</b>

A pointer to the string that receives the constructed root path. This buffer must be at least four characters in size.


## -returns



Type: <b>LPTSTR</b>

Returns the address of the constructed root path. If the call fails for any reason (for example, an invalid drive number), <i>szRoot</i> is returned unchanged.



