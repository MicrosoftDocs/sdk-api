---
UID: NF:rpcndr.RpcSmClientFree
title: RpcSmClientFree function
author: windows-sdk-content
description: The RpcSmClientFree function frees memory returned from a client stub.
old-location: rpc\rpcsmclientfree.htm
old-project: Rpc
ms.assetid: b3e9a526-7b78-49a6-9550-e3f682cecfb8
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: RpcSmClientFree, RpcSmClientFree function [RPC], _rpc_rpcsmclientfree, rpc.rpcsmclientfree, rpcndr/RpcSmClientFree
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcSmClientFree
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcSmClientFree function


## -description


The 
<b>RpcSmClientFree</b> function frees memory returned from a client stub.


## -parameters




### -param pNodeToFree

TBD




#### - NodeToFree

Pointer to memory returned from a client stub.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcSmClientFree</b> function releases memory allocated and returned from a client stub. The memory management handle of the thread calling this function must match the handle of the thread that made the RPC call. Use 
<a href="https://msdn.microsoft.com/5bf2c93c-8273-484b-a79f-821b2068692d">RpcSmGetThreadHandle</a> and 
<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a> to pass handles from thread to thread.

Note that using 
<b>RpcSmClientFree</b> allows a function to free dynamically-allocated memory returned by an RPC call without knowing the memory-management environment from which it was called.




## -see-also




<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a>



<a href="https://msdn.microsoft.com/5bf2c93c-8273-484b-a79f-821b2068692d">RpcSmGetThreadHandle</a>



<a href="https://msdn.microsoft.com/f6b6db72-c9af-44d1-9f84-26aaaa17691c">RpcSmSetClientAllocFree</a>



<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a>



<a href="https://msdn.microsoft.com/f07df5ec-0798-4cd2-a2f5-73e6245a7020">RpcSmSwapClientAllocFree</a>
 

 

