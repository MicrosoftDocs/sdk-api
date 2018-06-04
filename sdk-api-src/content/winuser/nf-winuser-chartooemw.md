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

# CharToOemW function


## -description


Translates a string into the OEM-defined character set.
<div class="alert"><b>Warning</b>  Do not use. See Security Considerations.</div><div> </div>

## -parameters




### -param pSrc

TBD


### -param pDst

TBD




#### - lpszDst [out]

Type: <b>LPSTR</b>

The destination buffer, which receives the translated string. If the <b>CharToOem</b> function is being used as an ANSI function, the string can be translated in place by setting the 
					<i>lpszDst</i> parameter to the same address as the 
					<i>lpszSrc</i> parameter. This cannot be done if <b>CharToOem</b> is being used as a wide-character function. 


#### - lpszSrc [in]

Type: <b>LPCTSTR</b>

The null-terminated string to be translated.


## -returns



Type: <b>BOOL</b>

The return value is always nonzero except when you pass the same address to 
						<i>lpszSrc</i> and 
						<i>lpszDst</i> in the wide-character version of the function. In this case the function returns zero and 
						<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INVALID_ADDRESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/5b9a968f-c325-48a1-bcc8-79aa5f286bdf">CharToOemBuff</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/2336b758-7b57-44d2-b3ce-34054128a26d">OemToChar</a>



<a href="https://msdn.microsoft.com/17b01f13-6c09-43e2-984c-3b085f6b353f">OemToCharBuff</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>
 

 

