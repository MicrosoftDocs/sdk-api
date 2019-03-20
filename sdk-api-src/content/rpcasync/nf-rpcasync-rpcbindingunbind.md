---
UID: NF:rpcasync.RpcBindingUnbind
title: RpcBindingUnbind function (rpcasync.h)
author: windows-sdk-content
description: Unbinds a binding handle previously bound by RpcBindingBind.
old-location: rpc\rpcbindingunbind.htm
tech.root: Rpc
ms.assetid: a9e30764-22ea-4dbf-9311-f37bd55ed2c4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcBindingUnbind, RpcBindingUnbind function [RPC], rpc.rpcbindingunbind, rpcasync/RpcBindingUnbind
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
 - RpcBindingUnbind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcBindingUnbind function


## -description


The <b>RpcBindingUnbind</b> function unbinds a binding handle previously bound by <a href="https://msdn.microsoft.com/dbc73a66-b1ca-4a53-b662-430b611f8c20">RpcBindingBind</a>.


## -parameters




### -param Binding [in]


<a href="https://msdn.microsoft.com/3e07d9e9-04d8-4f94-8104-cd0ee89a9407">RPC_BINDING_HANDLE</a> structure that contains the binding handle to unbind from the RPC server.


## -returns



This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcBindingUnbind</b> unbinds a previously bound binding handle from an RPC server. An unbound handle can be modified with calls like <a href="https://msdn.microsoft.com/bc721fb0-2271-4658-995b-a41e8eefc5d5">RpcBindingSetOption</a> and <a href="https://msdn.microsoft.com/2438816c-995e-4398-999d-48a3538eec18">RpcBindingSetAuthInfoEx</a>. A binding handle in the unbound state can be bound again and re-used to make calls.

The results of an unbind operation are undefined if it is called on a binding handle that currently has RPC calls in progress at the time of unbinding. It is the responsibility of the caller to ensure that no calls are in progress at the time an unbind operation is attempted.

Note that calling <b>RpcBindingUnbind</b> does not necessarily disconnect the client from the server. It will invalidate any cached information used by the binding handle, but actually disconnection is not ensured. To ensure disconnection, free the binding handle with <a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a>.

<b>Windows Vista:  </b>Currently, this function supports only the <b>ncalrpc</b> protocol sequence.




## -see-also




<a href="https://msdn.microsoft.com/dbc73a66-b1ca-4a53-b662-430b611f8c20">RpcBindingBind</a>



<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a>
 

 

