---
UID: NF:rpcdce.RpcSsDontSerializeContext
title: RpcSsDontSerializeContext function
author: windows-sdk-content
description: The RpcSsDontSerializeContext function disables run-time serialization of multiple calls dispatched to server-manager routines on the same context handle.
old-location: rpc\rpcssdontserializecontext.htm
tech.root: rpc
ms.assetid: 75c8bf34-1522-4db2-9c33-e1ca5ac11e4c
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: RpcSsDontSerializeContext, RpcSsDontSerializeContext function [RPC], _rpc_rpcssdontserializecontext, rpc.rpcssdontserializecontext, rpcdce/RpcSsDontSerializeContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcSsDontSerializeContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcSsDontSerializeContext function


## -description


The 
<b>RpcSsDontSerializeContext</b> function disables run-time serialization of multiple calls dispatched to server-manager routines on the same context handle. Use of this function is not recommended. Developers should use mixed mode–content handle serialization instead. The See Also section provides links to more appropriate functions.


## -parameters






## -returns



This function does not return a value.




## -remarks



The 
<b>RpcSsDontSerializeContext</b> function prevents the run time from performing this serialization service, allowing multiple calls to be dispatched on a given context handle. Calling this function does not disable serialization entirely—when a context run down occurs, your context run-down routine will not run until all outstanding client requests have completed. Changes to the context handle state, including freeing the context handle typically, must continue to be serialized.

It is recommended that, if your distributed application invokes the 
<b>RpcSsDontSerializeContext</b> function, the call should be made before the server program begins handling remote procedure calls.

<div class="alert"><b>Note</b>  Typically, the RPC run-time serializes calls on the same context handle dispatched to server manager routines. Context handles are maintained on a per-client basis and typically represent the server-side state. This means that your server manager does not have to guard against another thread from the same client changing the context or against the context running down while a call is dispatched.</div>
<div> </div>
<div class="alert"><b>Note</b>  After it is called, the 
<b>RpcSsDontSerializeContext</b> function is not revertible for the life of the process.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/192be467-b1e0-422b-878a-738cb7d72b5b">Multithreaded Clients and Context Handles</a>



<a href="https://msdn.microsoft.com/7ef2376b-da25-4e4b-8a25-0913d680945f">RpcSsContextLockExclusive</a>



<a href="https://msdn.microsoft.com/469f0995-54ff-40a6-9322-3d173e2c9861">RpcSsContextLockShared</a>



<a href="https://msdn.microsoft.com/b39654e4-6f03-43a0-8a5d-6f24bd0a529c">Server
		  Context Run-down Routine</a>



<a href="https://msdn.microsoft.com/aff2484e-639b-41d2-94a9-f34ca4f2343c">context_handle_noserialize</a>



<a href="https://msdn.microsoft.com/e2f48582-228a-4725-9543-1e638d86ff6b">context_handle_serialize</a>
 

 

