---
UID: NF:rpcasync.RpcBindingBind
title: RpcBindingBind function
author: windows-sdk-content
description: The RpcBindingBind function contacts an RPC server and binds to it.
old-location: rpc\rpcbindingbind.htm
tech.root: rpc
ms.assetid: dbc73a66-b1ca-4a53-b662-430b611f8c20
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: RpcBindingBind, RpcBindingBind function [RPC], rpc.rpcbindingbind, rpcasync/RpcBindingBind
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps \| UWP apps]
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
 - RpcBindingBind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcBindingBind function


## -description


The <b>RpcBindingBind</b> function contacts an RPC server and binds to it.


## -parameters




### -param pAsync [in, optional]

Pointer to the 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a> structure that contains asynchronous call information. This state information contains the completion method used to signal when the bind operation is complete.


### -param Binding [in]


<a href="https://msdn.microsoft.com/3e07d9e9-04d8-4f94-8104-cd0ee89a9407">RPC_BINDING_HANDLE</a> structure that contains the binding handle created with a previous call to <a href="https://msdn.microsoft.com/0188512e-bff6-414b-a6eb-19bfe8e0b3a9">RpcBindingCreate</a>.


### -param IfSpec [in]


<a href="https://msdn.microsoft.com/a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d">RPC_IF_HANDLE</a> value that specifies the interface on which calls for this binding handle will be made. 


## -returns



This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned. For information on these error codes, see <a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The RPC is successfully bound to the server and remote calls can be made.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
An obsolete feature of RPC was requested for this binding operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcBindingBind</b> contacts the RPC server and binds to it using the binding handle returned by a previous call to <a href="https://msdn.microsoft.com/0188512e-bff6-414b-a6eb-19bfe8e0b3a9">RpcBindingCreate</a>. Binding handles established using this method are referred to as "fast" binding handles.

If the value of the <i>pAsync</i> parameter is not <b>NULL</b>, then the bind will be asynchronous and calls to <a href="https://msdn.microsoft.com/e55d586f-969b-4e9a-97d9-b6c74b2a8b6d">RpcAsyncCancelCall</a> and <a href="https://msdn.microsoft.com/caa3add7-d07f-4d56-ad96-51dc67f66117">RpcAsyncGetCallStatus</a> can be made on the supplied async state. The completion method specified in the async state information wis used to signal the caller that the bind is complete. Upon notification of completion, calls can be made using the newly-bound binding handle.

The bind method does not determine what calls can be made using the binding handle — if the bind is synchronous, asynchronous calls can still be made on the binding handle, and vice versa. The bind method determines how notification for a successful bind is signaled, specifically in the case of asynchronous binds.

Since this API exchanges messages with the RPC server, bind operations can take a long time based on a number of independent factors including network traffic and server blocking. If the binding is synchronous, the bind operation can block if the server is blocked.

After the bind is complete, the semantics of calls made on the binding handle are the same as calls made on any other type of binding handle, but with four notable differences, listed below:


<ul>
<li>All calls on this binding handle must be made on the interface specified in <i>IfSpec</i>. The binding handle is uniquely tied to this interface. The interface itself can be unloaded before the binding handle is destroyed, but extensive information about the interface is cached in the binding handle, and if a call is made on the same binding handle for a different interface, the results are undefined.</li>
<li>RPC callbacks are not allowed on a binding handle. If the RPC server attempts to make a callback using a method with the [callback] attribute, the call is rejected with the RPC_S_CANNOT_SUPPORT error status code.</li>
<li>With classic binding handles, RPC will attempt to transparently reconnect with the server  if the connection is dropped. For fast binding handles, RPC will not attempt to transparently reconnect to the server; instead, it  will return one of the following errors: RPC_S_SERVER_UNAVAILABLE, RPC_S_CALL_FAILED, and RPC_C_CALL_FAILED_DNE.  If the connection is dropped due to rejected credentials, RPC_S_ACCESS_DENIED is returned; and if the server encounters a transient error due to a lack of memory, RPC_S_OUT_OF_MEMORY is returned. Any other connectivity errors are the result of marshaling or unmarshaling errors returned by server routines.In the case of a lost connection, the called must unbind by calling <a href="https://msdn.microsoft.com/a9e30764-22ea-4dbf-9311-f37bd55ed2c4">RpcBindingUnbind</a> and then rebind with another call to <b>RpcBindingBind</b>.

</li>
</ul>


If the call to <b>RpcBindingBind</b> fails, then the binding handle is not bound to the server and the caller can attempt to bind again with another call to the same API, or it can free the binding handle. Since a failed bind operation does not move the binding handle to the bound state, <a href="https://msdn.microsoft.com/a9e30764-22ea-4dbf-9311-f37bd55ed2c4">RpcBindingUnbind</a> must not be called on it.

Certain functions must not be called until the bind operation has signaled completion, specifically:<ul>
<li>
<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2f7a447a-50b1-422e-a49a-00ede3fcf187">RpcBindingReset</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2db946b6-6a0d-402c-89ef-68c7489aa7ee">RpcBindingSetAuthInfo</a> and <a href="https://msdn.microsoft.com/2438816c-995e-4398-999d-48a3538eec18">RpcBindingSetAuthInfoEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5dcf341f-e392-4608-b741-8fa07cabd50b">RpcBindingSetObject</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bc721fb0-2271-4658-995b-a41e8eefc5d5">RpcBindingSetOption</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3ea6fe6a-2064-4f53-852a-041281b62bbd">RpcMgmtSetComTimeout</a>
</li>
</ul>


<div class="alert"><b>Note</b>  Currently, this function supports only the <b>ncalrpc</b> protocol sequence.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0188512e-bff6-414b-a6eb-19bfe8e0b3a9">RpcBindingCreate</a>



<a href="https://msdn.microsoft.com/a9e30764-22ea-4dbf-9311-f37bd55ed2c4">RpcBindingUnbind</a>
 

 

