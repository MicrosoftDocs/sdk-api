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

# PathIsUNCEx function


## -description



Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.

This function differs from <a href="https://msdn.microsoft.com/53da5ba7-a2a4-45b2-90e0-ae006415933e">PathIsUNC</a> in that it also allows you to extract the name of the server from the path.




## -parameters




### -param pszPath [in]

A pointer to the path string.


### -param ppszServer [out, optional]

A pointer to a string that, when this function returns successfully, receives the server portion of the UNC path. This value can be <b>NULL</b> if you don't need this information.


## -returns



Returns <b>TRUE</b> if the string is a valid UNC path; otherwise, <b>FALSE</b>.



