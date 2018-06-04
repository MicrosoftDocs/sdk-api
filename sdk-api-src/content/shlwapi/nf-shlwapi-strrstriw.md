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

# StrRStrIW function


## -description


Searches for the last occurrence of a specified substring within a string. The comparison is not case-sensitive.


## -parameters




### -param pszSource [in]

Type: <b>PTSTR</b>

A pointer to a <b>null</b>-terminated source string.


### -param pszLast [in, optional]

Type: <b>PCTSTR</b>

A pointer into the source string that defines the range of the search. Set <i>pszLast</i> to point to a character in the source string, and the search will stop with the preceding character. Set <i>pszLast</i> to <b>NULL</b> to search the entire source string.


### -param pszSrch [in]

Type: <b>PCTSTR</b>

A pointer to the substring to search for.


## -returns



Type: <b>PTSTR</b>

Returns the address of the last occurrence of the substring if successful, or <b>NULL</b> otherwise.



