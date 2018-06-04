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

# LdapUnicodeToUTF8 function


## -description


The <b>LdapUnicodeToUTF8</b> function converts Unicode strings to UTF-8. Modules that do not have the UTF-8 code page can call this function.


## -parameters




### -param lpSrcStr [in]

A pointer to a null-terminated Unicode string to convert.


### -param cchSrc [in]

An integer that specifies the size, in characters, of the <i>lpSrcStr</i> string.


### -param lpDestStr [out]

A pointer to a buffer that receives the converted UTF-8 character string, without a null terminator.


### -param cchDest [in]

An integer that specifies the size, in characters, of the <i>lpDestStr</i> buffer.


## -returns



The return value is the size, in characters, written to the <i>lpDestStr</i> buffer.
      If the <i>lpDestStr</i> buffer is too small, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>.

When the <i>cchDest</i> parameter is zero, the required size of the destination buffer is returned.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/4c36ce90-8cc6-4dee-b990-5d283613ba11">LdapUTF8ToUnicode</a>
 

 

