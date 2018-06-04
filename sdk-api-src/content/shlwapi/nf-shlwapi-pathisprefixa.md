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

# PathIsPrefixA function


## -description


Searches a path to determine if it contains a valid prefix of the type passed by <i>pszPrefix</i>. A prefix is one of these types: "C:\\", ".", "..", "..\\".


## -parameters




### -param pszPrefix [in]

Type: <b>IN LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the prefix for which to search.


### -param pszPath [in]

Type: <b>IN LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be searched.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the compared path is the full prefix for the path, or <b>FALSE</b> otherwise.



