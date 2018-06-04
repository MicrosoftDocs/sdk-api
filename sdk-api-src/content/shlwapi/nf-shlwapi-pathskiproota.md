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

# PathSkipRootA function


## -description


Retrieves a pointer to the first character in a path following the drive letter or Universal Naming Convention (UNC) server/share path elements.


## -parameters




### -param pszPath [in]

Type: <b>PTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to parse.


## -returns



Type: <b>PTSTR</b>

A pointer that, when this function returns successfully, points to the beginning of the subpath that follows the root (drive letter or UNC server/share). If the function encounters an error, this value will be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/187bc49e-c5ae-42b8-acbd-a765f871d73b">PathCchSkipRoot</a>
 

 

