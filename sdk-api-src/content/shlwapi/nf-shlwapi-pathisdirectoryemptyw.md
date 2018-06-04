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

# PathIsDirectoryEmptyW function


## -description


Determines whether a specified path is an empty directory.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be tested.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>pszPath</i> is an empty directory. Returns <b>FALSE</b> if <i>pszPath</i> is not a directory, or if it contains at least one file other than "." or "..".




## -remarks



"C:\" is considered a directory.




## -see-also




<a href="https://msdn.microsoft.com/9af3e3da-6b3a-4e81-ba50-ff7aeeb73c44">PathIsDirectory</a>
 

 

