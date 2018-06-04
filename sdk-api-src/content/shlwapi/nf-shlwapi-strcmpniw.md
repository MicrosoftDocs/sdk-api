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

# StrCmpNIW function


## -description


Compares a specified number of characters from the beginning of two strings to determine if they are the same. The comparison is not case-sensitive. The <b>StrNCmpI</b> macro differs from this function in name only.


## -parameters




### -param psz1 [in]

Type: <b>PCTSTR</b>

A pointer to the first null-terminated string to be compared.


### -param psz2 [in]

Type: <b>PCTSTR</b>

A pointer to the second null-terminated string to be compared.


### -param nChar [in]

Type: <b>int</b>

The number of characters from the beginning of each string to be compared.


## -returns



Type: <b>int</b>

Returns zero if the strings are identical. Returns a positive value if the first <i>nChar</i> characters of the string pointed to by <i>psz1</i> are greater than those from the string pointed to by <i>psz2</i>. It returns a negative value if the first <i>nChar</i> characters of the string pointed to by <i>psz1</i> are less than those from the string pointed to by <i>psz2</i>.



