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

# StrPBrkA function


## -description


Searches a string for the first occurrence of a character contained in a specified buffer. This search does not include the terminating null character.


## -parameters




### -param psz [in]

Type: <b>PTSTR</b>

A pointer to the null-terminated string to be searched.


### -param pszSet [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated character buffer that contains the characters for which to search.


## -returns



Type: <b>PTSTR</b>

Returns the address in <i>psz</i> of the first occurrence of a character contained in the buffer at <i>pszSet</i>, or <b>NULL</b> if no match is found.



