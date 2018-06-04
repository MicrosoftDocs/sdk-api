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

# PathSearchAndQualifyW function


## -description


Determines if a given path is correctly formatted and fully qualified.


## -parameters




### -param pszPath

TBD


### -param pszBuf

TBD


### -param cchBuf

TBD




#### - cchFullyQualifiedPath [in]

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszFullyQualifiedPath</i>, in characters.


#### - pcszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to search.


#### - pszFullyQualifiedPath [out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be referenced.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the path is qualified, or <b>FALSE</b> otherwise.



