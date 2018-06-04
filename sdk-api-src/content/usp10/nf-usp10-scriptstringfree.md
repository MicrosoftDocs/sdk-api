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

# ScriptStringFree function


## -description


Frees a <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure.


## -parameters




### -param pssa [in, out]

Pointer to a <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure.


## -returns



Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



When your application is finished with a <a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a> structure, it should free the associated memory by calling this function. After this function is called, the pointers retrieved from <a href="https://msdn.microsoft.com/ad3f15cc-d4e9-4e71-a8c8-287bd62e9b15">ScriptString_pcOutChars</a>, <a href="https://msdn.microsoft.com/ff898c79-2d37-4c0b-af83-2322ab7cf656">ScriptString_pLogAttr</a>, and <a href="https://msdn.microsoft.com/2938e600-3f6b-4178-bc0f-bcbcd97b9d04">ScriptString_pSize</a> that are associated with the <i>pssa</i> parameter are invalid.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aa93d631-3cfc-449d-9d04-c1f851129c6c">SCRIPT_STRING_ANALYSIS</a>



<a href="https://msdn.microsoft.com/ff898c79-2d37-4c0b-af83-2322ab7cf656">ScriptString_pLogAttr</a>



<a href="https://msdn.microsoft.com/2938e600-3f6b-4178-bc0f-bcbcd97b9d04">ScriptString_pSize</a>



<a href="https://msdn.microsoft.com/ad3f15cc-d4e9-4e71-a8c8-287bd62e9b15">ScriptString_pcOutChars</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

