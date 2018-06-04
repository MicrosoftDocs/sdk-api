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

# InitOnceExecuteOnce function


## -description


Executes the specified function successfully one time. No other threads that specify the same one-time initialization structure can execute the specified function while it is being executed by the current thread.


## -parameters




### -param InitOnce [in, out]

A pointer to the one-time initialization structure.


### -param InitFn [in]

A pointer to an application-defined <a href="https://msdn.microsoft.com/e4a73572-e477-4518-87fe-b9b74234e8ec">InitOnceCallback</a> function.


### -param Context [out, optional]

A parameter that receives data stored with the one-time initialization structure upon success. The low-order <b>INIT_ONCE_CTX_RESERVED_BITS</b> bits of the data are always zero.


### -param Parameter [in, out, optional]

A parameter to be passed to the callback function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is used for synchronous one-time initialization. For asynchronous one-time initialization, use the <a href="https://msdn.microsoft.com/f342e85c-ac81-4470-89ce-a9d0fc5e8f89">InitOnceBeginInitialize</a> function with the <b>INIT_ONCE_ASYNC</b> flag.

Only one thread at a time can execute the callback function specified by <i>InitFn</i>. Other threads that specify the same one-time initialization structure block until the callback finishes.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example that uses 
this function, see 
<a href="https://msdn.microsoft.com/47e68fbb-29f8-4930-beba-01d44263eb1e">Using One-Time Initialization</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e4a73572-e477-4518-87fe-b9b74234e8ec">InitOnceCallback</a>



<a href="https://msdn.microsoft.com/f2943ac5-0e43-4f07-8941-952383e2fa08">InitOnceInitialize</a>



<a href="https://msdn.microsoft.com/404c083c-7bee-44c2-b8e7-da1901b6ab2f">One-Time Initialization</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

