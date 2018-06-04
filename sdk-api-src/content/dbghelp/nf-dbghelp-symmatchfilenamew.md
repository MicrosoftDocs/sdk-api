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

# SymMatchFileNameW function


## -description


Compares a string to a file name and path.


## -parameters




### -param FileName [in]

The file name to be compared to the <i>Match</i> parameter.


### -param Match [in]

The string to be compared to the <i>FileName</i> parameter.


### -param FileNameStop [out, optional]

A pointer to a string buffer that receives a pointer to the location in <i>FileName</i> where matching stopped. For a complete match, this value can be one character before <i>FileName</i>. This value can also be <b>NULL</b>.


### -param MatchStop [out, optional]

A pointer to a string buffer that receives a pointer to the location in <i>Match</i> where matching stopped. For a complete match, this value may be one character before <i>Match</i>. This value may be <b>NULL</b>.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Because the match string can be a suffix of the complete file name, this function can be used to match a plain file name to a fully qualified file name.

Matching begins from the end of both strings and proceeds backward. Matching is case-insensitive and equates a backslash ('\') with a forward slash ('/').

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

