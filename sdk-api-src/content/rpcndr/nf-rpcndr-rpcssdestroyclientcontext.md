---
UID: NF:rpcndr.RpcSsDestroyClientContext
title: RpcSsDestroyClientContext function
author: windows-driver-content
description: The RpcSsDestroyClientContext function destroys a context handle no longer needed by the client, without contacting the server.
old-location: rpc\rpcssdestroyclientcontext.htm
old-project: Rpc
ms.assetid: 7c4fe939-eda9-45c3-84fb-491ac96e7c78
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: RpcSsDestroyClientContext, RpcSsDestroyClientContext function [RPC], _rpc_rpcssdestroyclientcontext, rpc.rpcssdestroyclientcontext, rpcndr/RpcSsDestroyClientContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcSsDestroyClientContext
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

