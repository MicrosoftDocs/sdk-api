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

# UrlCompareA function


## -description


Makes a case-sensitive comparison of two URL strings.


## -parameters




### -param psz1 [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the first URL.


### -param psz2 [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the second URL.


### -param fIgnoreSlash

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> to have <b>UrlCompare</b> ignore a trailing '/' character on either or both URLs.


## -returns



Type: <b>int</b>

Returns zero if the two strings are equal. The function will also return zero if <i>fIgnoreSlash</i> is set to <b>TRUE</b> and one of the strings has a trailing '\' character. The function returns a negative integer if the string pointed to by <i>psz1</i> is less than the string pointed to by <i>psz2</i>. Otherwise, it returns a positive integer.




## -remarks



For best results, you should first canonicalize the URLs with <a href="https://msdn.microsoft.com/70802745-0611-4d37-800e-b50d5ea23426">UrlCanonicalize</a>. Then, compare the canonicalized URLs with <b>UrlCompare</b>.




## -see-also




<a href="https://msdn.microsoft.com/12530a04-776c-4506-86d1-07e2c3569a36">StrCmp</a>
 

 

