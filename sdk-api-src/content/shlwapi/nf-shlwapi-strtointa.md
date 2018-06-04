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

# StrToIntA function


## -description


Converts a string that represents a decimal value to an integer. The <b>StrToLong</b> macro is identical to this function.


## -parameters




### -param pszSrc [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated string to be converted. A valid string representing a decimal value contains only the characters 0-9 and must have the following form to be parsed successfully.
                    
                    

<pre class="syntax" xml:space="preserve"><code>(optional white space)(optional sign)(one or more decimal digits)</code></pre>
The optional sign can be the character '-' or '+'; if omitted, the sign is assumed to be positive.


## -returns



Type: <b>int</b>

Returns the <b>int</b> value represented by <i>pszSrc</i>. For instance, the string "123" returns the integer value 123.




## -remarks



If the string pointed to by <i>pszSrc</i> contains an invalid character, that character is considered the end of the string to be converted and the remainder is ignored. For instance, given the invalid decimal string "12b34", <b>StrToInt</b> only recognizes "12" and returns that integer value.




## -see-also




<a href="https://msdn.microsoft.com/2e8286c7-585f-441b-904b-f3b4e8cf95f9">StrToIntEx</a>
 

 

