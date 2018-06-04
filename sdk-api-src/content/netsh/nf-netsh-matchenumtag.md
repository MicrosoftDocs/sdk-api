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

# MatchEnumTag function


## -description


The 
<b>MatchEnumTag</b> function searches a table of legal values to find a value that matches a specific token. The 
<b>MatchEnumTag</b> function is typically called by a command function when an argument is specified that has an enumerated set of possible values.


## -parameters




### -param hModule

Reserved. Set to null.


### -param pwcArg [in]

A token to match. The <i>pwcArg</i> parameter is usually an entry in the <i>ppwcArguments</i> array passed into the 
<a href="https://msdn.microsoft.com/5058e202-9ad4-4789-97db-3c13b4a1c337">FN_HANDLE_CMD</a> function exposed by the helper (the command function).


### -param dwNumArg [in]

The number of entries in the <i>pEnumTable</i> array.


### -param pEnumTable [in]

An array of token:value pairs.


### -param pdwValue [out]

Upon success, the <i>pdwValue</i> parameter is filled with the value associated with the token in the <i>pEnumTable</i> array.


## -see-also




<a href="https://msdn.microsoft.com/5058e202-9ad4-4789-97db-3c13b4a1c337">FN_HANDLE_CMD</a>
 

 

