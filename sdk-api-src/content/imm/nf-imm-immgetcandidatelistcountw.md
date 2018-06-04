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

# ImmGetCandidateListCountW function


## -description


Retrieves the size of the candidate lists.


## -parameters




### -param HIMC

TBD


### -param lpdwListCount [out]

Pointer to the buffer in which this function retrieves the size of the candidate lists.


#### - hIMC [in]

Handle to the input context.


## -returns



Returns the number of bytes required for all candidate lists if successful, or 0 otherwise.




## -remarks



Applications typically call this function in response to an <a href="https://msdn.microsoft.com/439ff125-2731-4eb1-8287-4ca8ace7d8ec">IMN_OPENCANDIDATE</a> or <a href="https://msdn.microsoft.com/0a276f9c-cece-4fa6-b71a-ba0daad5ca05">IMN_CHANGECANDIDATE</a> command.




## -see-also




<a href="https://msdn.microsoft.com/0a276f9c-cece-4fa6-b71a-ba0daad5ca05">IMN_CHANGECANDIDATE</a>



<a href="https://msdn.microsoft.com/439ff125-2731-4eb1-8287-4ca8ace7d8ec">IMN_OPENCANDIDATE</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

