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

# PathCchSkipRoot function


## -description



Retrieves a pointer to the first character in a path following the drive letter or Universal Naming Convention (UNC) server/share path elements.

This function differs from <a href="https://msdn.microsoft.com/528a3953-26d7-4fff-be31-9c9788d429ab">PathSkipRoot</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.




## -parameters




### -param pszPath [in]

A pointer to the path string.


### -param ppszRootEnd [out]

The address of a pointer that, when this function returns successfully, points to the first character in a path following the drive letter or UNC server/share path elements. If the path consists of only a root, this value will point to the string's terminating null character.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



