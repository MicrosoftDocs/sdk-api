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

# ImmSetCandidateWindow function


## -description


Sets information about the candidates window.


## -parameters




### -param HIMC

TBD


### -param lpCandidate [in]

Pointer to a <a href="https://msdn.microsoft.com/86edcfe0-07f7-4bd7-9444-3a884aeb7926">CANDIDATEFORM</a> structure that contains information about the candidates window.


#### - hIMC [in]

Handle to the input context.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function causes an <a href="https://msdn.microsoft.com/64252d88-130b-44c3-854a-78b01def7a13">IMN_SETCANDIDATEPOS</a> command to be sent. Both the IME and the application call this function.




## -see-also




<a href="https://msdn.microsoft.com/86edcfe0-07f7-4bd7-9444-3a884aeb7926">CANDIDATEFORM</a>



<a href="https://msdn.microsoft.com/64252d88-130b-44c3-854a-78b01def7a13">IMN_SETCANDIDATEPOS</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

