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

# ImmSetConversionStatus function


## -description


Sets the current conversion status.


## -parameters




### -param HIMC

TBD


### -param DWORD

TBD




#### - fdwConversion [in]

Conversion mode values. For more information, see <a href="https://msdn.microsoft.com/0b0afb4e-f7aa-4ca6-9174-21983b2a422b">IME Conversion Mode Values</a>.


#### - fdwSentence [in]

Sentence mode values. For more information, see <a href="https://msdn.microsoft.com/24b12936-7dfc-4c8d-970c-d8354ad46d1d">IME Sentence Mode Values</a>.


#### - hIMC [in]

Handle to the input context.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function sends the <a href="https://msdn.microsoft.com/62bb9717-cc41-4e34-af1a-ff41324bd3a9">IMN_SETCONVERSIONMODE</a> and <a href="https://msdn.microsoft.com/72455193-cd17-45f8-b19c-a1f735ff81bf">IMN_SETSENTENCEMODE</a> commands to the application.

<div class="alert"><b>Note</b>  <b>Beginning with Windows 8:</b> By default, the input switch is set per user instead of per thread. 
The Microsoft IME (Japanese) respects the mode globally, and therefore  <b>ImmSetConversionStatus</b> fails when getting focus.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/62bb9717-cc41-4e34-af1a-ff41324bd3a9">IMN_SETCONVERSIONMODE</a>



<a href="https://msdn.microsoft.com/72455193-cd17-45f8-b19c-a1f735ff81bf">IMN_SETSENTENCEMODE</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

