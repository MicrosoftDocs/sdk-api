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

# StrTrimW function


## -description


Removes specified leading and trailing characters from a string.


## -parameters




### -param psz [in, out]

Type: <b>PTSTR</b>

A pointer to the null-terminated string to be trimmed. When this function returns successfully, <i>psz</i> receives the trimmed string.


### -param pszTrimChars [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string that contains the characters to trim from <i>psz</i>.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if any characters were removed; otherwise, <b>FALSE</b>.



