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

# ImmGetConversionStatus function


## -description


Retrieves the current conversion status.


## -parameters




### -param HIMC

TBD


### -param lpfdwConversion [out, optional]

Pointer to a variable in which the function retrieves a combination of conversion mode values. For more information, see <a href="https://msdn.microsoft.com/0b0afb4e-f7aa-4ca6-9174-21983b2a422b">IME Conversion Mode Values</a>.


### -param lpfdwSentence [out, optional]

Pointer to a variable in which the function retrieves a sentence mode value. For more information, see <a href="https://msdn.microsoft.com/24b12936-7dfc-4c8d-970c-d8354ad46d1d">IME Sentence Mode Values</a>.


#### - hIMC [in]

Handle to the input context for which to retrieve status information.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



Conversion and sentence mode values are set only if the IME supports those modes.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

