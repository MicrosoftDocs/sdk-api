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

# RpcSsSetThreadHandle function


## -description


The 
<b>RpcSsSetThreadHandle</b> function sets a thread handle for the stub memory–management environment.


## -parameters




### -param Id

TBD




#### - Handle

Thread handle returned by a call to 
<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a>.


## -returns



This function does not return a value.




## -remarks



An application calls 
<b>RpcSsSetThreadHandle</b> to set a thread handle for the stub memory–management environment. A thread used to manage memory for the stub memory–management environment calls 
<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a> to obtain a handle for its memory environment. In this way, another thread that calls 
<b>RpcSsSetThreadHandle</b> by using this handle can then use the same memory-management environment.

The same thread handle must be used by multiple threads calling 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a> and 
<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a> in order to manage the same memory. Before spawning new threads to manage the same memory, the thread that established the memory-management environment (parent thread) calls 
<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a> to obtain a thread handle for this environment. Then, the spawned threads call 
<b>RpcSsSetThreadHandle</b> with the handle provided by the parent thread.

Typically, a thread spawned by a server manager procedure calls 
<b>RpcSsSetThreadHandle</b>. The stub sets up the memory-management environment for the manager procedure, and the manager calls 
<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a> to obtain a thread handle. Then, each spawned thread calls 
<b>RpcSsGetThreadHandle</b> to get access to the manager's memory-management environment.

A thread can also call 
<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a> and 
<b>RpcSsSetThreadHandle</b> to save and restore its memory-management environment.

<div class="alert"><b>Note</b>  The 
<b>RpcSsSetThreadHandle</b> routine raises exceptions, while the 
<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a> routine returns the error code.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a>



<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>



<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a>



<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a>
 

 

