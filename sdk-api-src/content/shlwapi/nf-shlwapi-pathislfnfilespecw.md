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

# PathIsLFNFileSpecW function


## -description


Determines whether a file name is in long format.


## -parameters




### -param pszName [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the file name to be tested.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>pszName</i> exceeds the number of characters allowed by the 8.3 format, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/c69d6cca-44e7-4792-8fb2-3c4ecd2e57f2">PathIsFileSpec</a>
 

 

