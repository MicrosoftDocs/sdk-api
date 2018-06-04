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

# OemToCharBuffW function


## -description


Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string.


## -parameters




### -param lpszSrc [in]

Type: <b>LPCSTR</b>

One or more characters from the OEM-defined character set.


### -param lpszDst [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the translated string. If the <b>OemToCharBuff</b> function is being used as an ANSI function, the string can be translated in place by setting the 
					<i>lpszDst</i> parameter to the same address as the 
					<i>lpszSrc</i> parameter. This cannot be done if the <b>OemToCharBuff</b> function is being used as a wide-character function.


### -param cchDstLength [in]

Type: <b>DWORD</b>

The number of 
					characters to be translated in the buffer identified by the 
					<i>lpszSrc</i> parameter.


## -returns



Type: <b>BOOL</b>

The return value is always nonzero except when you pass the same address to 
						<i>lpszSrc</i> and 
						<i>lpszDst</i> in the wide-character version of the function. In this case the function returns zero and 
						<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INVALID_ADDRESS</b>.




## -remarks



Unlike the <a href="https://msdn.microsoft.com/2336b758-7b57-44d2-b3ce-34054128a26d">OemToChar</a> function, the <b>OemToCharBuff</b> function does not stop converting characters when it encounters a null character in the buffer pointed to by 
				<i>lpszSrc</i>. The <b>OemToCharBuff</b> function converts all 
				<i>cchDstLength</i> characters.




## -see-also




<a href="https://msdn.microsoft.com/66588b51-1673-4cb0-828f-9e00de4a622e">CharToOem</a>



<a href="https://msdn.microsoft.com/5b9a968f-c325-48a1-bcc8-79aa5f286bdf">CharToOemBuff</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/2336b758-7b57-44d2-b3ce-34054128a26d">OemToChar</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>
 

 

