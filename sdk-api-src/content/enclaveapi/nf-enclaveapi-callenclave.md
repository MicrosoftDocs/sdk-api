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

# CallEnclave function


## -description


Calls a function within an enclave. <b>CallEnclave</b> can also be called within an enclave to call a function outside of the enclave.


## -parameters




### -param lpRoutine [in]

The address of the function that you want to call.


### -param lpParameter [in]

The parameter than you want to pass to the function.


### -param fWaitForThread [in]

<b>TRUE</b> if the call to the specified function should block execution until an idle enclave thread becomes available when no idle enclave thread is available. 
<b>FALSE</b> if the call to the specified function should fail when no idle enclave thread is available. 


This parameter is ignored when you use <b>CallEnclave</b> within an enclave to call a function that is not in any enclave.


### -param lpReturnValue [out]

The return value of the function, if it is called successfully.


## -returns



<b>TRUE</b> if the specified function was called successfully; otherwise <b>FALSE</b>. To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<a href="https://msdn.microsoft.com/D2BAF02F-AE05-43F2-BDB1-013EAF3AC653">TerminateEnclave</a>
 

 

