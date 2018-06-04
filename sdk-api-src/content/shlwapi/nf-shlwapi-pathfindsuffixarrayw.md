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

# PathFindSuffixArrayW function


## -description


Determines whether a given file name has one of a list of suffixes.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the file name to be tested. A full path can be used.


### -param apszSuffix [in]

Type: <b>const LPCTSTR*</b>

An array of <i>iArraySize</i> string pointers. Each string pointed to is null-terminated and contains one suffix. The strings can be of variable lengths.


### -param iArraySize [in]

Type: <b>int</b>

The number of elements in the array pointed to by <i>apszSuffix</i>.


## -returns



Type: <b>LPCTSTR</b>

Returns a pointer to a string with the matching suffix if successful, or <b>NULL</b> if <i>pszPath</i> does not end with one of the specified suffixes.




## -remarks



This function uses a case-sensitive comparison. The suffix must match exactly.



