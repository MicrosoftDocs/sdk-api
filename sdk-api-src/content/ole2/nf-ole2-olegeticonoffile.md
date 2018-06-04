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

# OleGetIconOfFile function


## -description


Returns a handle to a metafile containing an icon and string label for the specified file name.


## -parameters




### -param lpszPath [in]

A pointer to a file for which the icon and string are to be requested.


### -param fUseFileAsLabel [in]

Indicates whether to use the file name as the icon label.


## -returns



If the function succeeds, the return value is a handle to a metafile that contains and icon and label for the specified file. If there is no CLSID in the registration database for the file, then the function returns the string "Document". If <i>lpszPath</i> is <b>NULL</b>, the function returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/88ac1c14-b5a8-4100-9fa5-d7af35052b48">OleGetIconOfClass</a>



<a href="https://msdn.microsoft.com/627a79eb-46dd-4df7-a0d6-cab37b73387a">OleMetafilePictFromIconAndLabel</a>
 

 

