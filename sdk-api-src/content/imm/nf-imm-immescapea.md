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

# ImmEscapeA function


## -description


Accesses capabilities of particular IMEs that are not available through other IME API functions. This function is used mainly for country-specific operations.


## -parameters




### -param HKL

TBD


### -param HIMC

TBD


### -param UINT

TBD


### -param LPVOID

TBD




#### - hIMC [in]

Handle to the input context.


#### - hKL [in]

Input locale identifier.


#### - lpData [in, out]

Pointer to the data required for the escape specified in <i>uEscape</i>. On output, this parameter indicates the result of the escape. For more information, see <a href="https://msdn.microsoft.com/ede886dc-8a92-428c-8975-3feadc1d4f90">IME Escapes</a>.


#### - uEscape [in]

Index of the operations. For more information, see <a href="https://msdn.microsoft.com/ede886dc-8a92-428c-8975-3feadc1d4f90">IME Escapes</a>.


## -returns



Returns an operation-specific value if successful, or 0 otherwise.




## -remarks



When <i>uEscape</i> is set to IME_ESC_QUERY_SUPPORT, <i>lpData</i> indicates the buffer containing the IME escape value. For example, to see if the current IME supports IME_ESC_GETHELPFILENAME, your application uses the following call:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD dwEsc = IME_ESC_GETHELPFILENAME;
LRESULT lRet = ImmEscape(hKL,
                         hIMC,
                         IME_ESC_QUERY_SUPPORT,
                         (LPVOID)&amp;dwEsc);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

