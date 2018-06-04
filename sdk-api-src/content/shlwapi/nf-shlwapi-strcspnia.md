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

# StrCSpnIA function


## -description


Searches a string for the first occurrence of any of a group of characters. The search method is not case-sensitive, and the terminating <b>NULL</b> character is included within the search pattern match.


## -parameters




### -param pszStr [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated string to be searched.


### -param pszSet [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string containing the characters to search for.


## -returns



Type: <b>int</b>

Returns the index of the first occurrence in <i>pszStr</i> of any character from <i>pszSet</i>, or the length of <i>pszStr</i> if no match is found.




## -remarks



The return value of this function is equal to the length of the initial substring in <i>pszStr</i> that does not include any characters from <i>pszSet</i>.



