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

# RpcSsDestroyClientContext function


## -description


The 
<b>RpcSsDestroyClientContext</b> function destroys a context handle no longer needed by the client, without contacting the server.


## -parameters




### -param ContextHandle

Context handle to be destroyed. The handle is set to <b>NULL</b> before 
<b>RpcSsDestroyClientContext</b> returns.


## -returns



<b>RpcSsDestroyClientContext</b> has no return value.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcSsDestroyClientContext</b> is used by the client application to reclaim the memory resources used to maintain a context handle on the client. This function is used when <i>ContextHandle</i> is no longer valid, such as when a communication failure has occurred and the server is no longer available. The context handle is set to <b>NULL</b>. The 
<b>RpcSsDestroyClientContext</b> function provides the same functionality as the 
<a href="https://msdn.microsoft.com/ae886740-09e9-46a1-aa62-5dbcf6abab36">RpcSmDestroyClientContext</a> function. This function does not invoke the server's context handle run-down process.

Do not use 
<b>RpcSsDestroyClientContext</b> to replace a server function that closes the context handle.

The 
<b>RpcSsDestroyClientContext</b> function can throw an RPC_X_SS_CONTEXT_MISMATCH exception if the context handle passed to it is invalid. Applications should never pass an invalid context handle to this function. If an exception is thrown, it indicates an error in the calling code, and should therefore be investigated and fixed.




## -see-also




<a href="https://msdn.microsoft.com/2f7a447a-50b1-422e-a49a-00ede3fcf187">RpcBindingReset</a>



<a href="https://msdn.microsoft.com/ae886740-09e9-46a1-aa62-5dbcf6abab36">RpcSmDestroyClientContext</a>
 

 

