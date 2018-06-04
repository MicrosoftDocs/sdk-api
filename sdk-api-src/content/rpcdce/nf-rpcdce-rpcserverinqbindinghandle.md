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

# RpcServerInqBindingHandle function


## -description


The <b>RpcServerInqBindingHandle</b> function  obtains the binding handle for RPC calls serviced by the thread in which <b>RpcServerInqBindingHandle</b> is called.


## -parameters




### -param Binding


<a href="https://msdn.microsoft.com/3e07d9e9-04d8-4f94-8104-cd0ee89a9407">RPC_BINDING_HANDLE</a> structure that, upon success, receives the binding handle for the call serviced by the thread on which <b>RpcServerInqBindingHandle</b> is also called.

If the call fails, this parameter is undefined.


## -returns



This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned. This function cannot fail unless it is called on a thread that is not currently servicing an RPC call.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcServerInqBindingHandle</b> is used to obtain the binding handle for the RPC call that is currently executing on the thread from which this API is also called. Since many RPC APIs require a binding handle as input, this is a convenient way to obtain a binding handle.

Note that all server-side RPC APIs that take a binding handle as a parameter allow you to pass NULL as an accepted value. Passing NULL instead of a binding handle indicates  that the binding handle for the RPC call currently executing in the same thread should be used. However, if you call a server-side API from a separate thread, then you will need to supply a non-NULL binding handle to them.

If you use explicit binding handles and do not use thread-specific context handles, the binding handle for the call is the first parameter to your server manager routine. However, if you do not use explicit handles or if you use context handles, <b>RpcServerInqBindingHandle</b> is the only way to obtain a binding handle to use in another thread.

This API can be used for both asynchronous and synchronous calls, although it is less useful for asynchronous calls since the binding handle can be obtained as the async state is always the first parameter for all asynchronous RPC calls and the binding handle can be obtained directly from it using <a href="https://msdn.microsoft.com/5a218d25-187e-4899-8a27-a955f77af8c2">RpcAsyncGetCallHandle</a>.




## -see-also




<a href="https://msdn.microsoft.com/5a218d25-187e-4899-8a27-a955f77af8c2">RpcAsyncGetCallHandle</a>
 

 

