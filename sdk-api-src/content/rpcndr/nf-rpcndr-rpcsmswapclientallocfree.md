---
UID: NF:rpcndr.RpcSmSwapClientAllocFree
title: RpcSmSwapClientAllocFree function
author: windows-driver-content
description: The RpcSmSwapClientAllocFree function exchanges the client stub's memory-allocation and memory-freeing mechanisms with those supplied by the client.
old-location: rpc\rpcsmswapclientallocfree.htm
old-project: Rpc
ms.assetid: f07df5ec-0798-4cd2-a2f5-73e6245a7020
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: RpcSmSwapClientAllocFree, RpcSmSwapClientAllocFree function [RPC], _rpc_rpcsmswapclientallocfree, rpc.rpcsmswapclientallocfree, rpcndr/RpcSmSwapClientAllocFree
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
-	RpcSmSwapClientAllocFree
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcSmSwapClientAllocFree function


## -description


The 
<b>RpcSmSwapClientAllocFree</b> function exchanges the client stub's memory-allocation and memory-freeing mechanisms with those supplied by the client.


## -parameters




### -param ClientAlloc

TBD


### -param ClientFree

TBD


### -param OldClientAlloc

TBD


### -param OldClientFree

TBD




#### - pfnAllocate

New memory-allocation function.


#### - pfnFree

New memory-releasing function.


#### - pfnOldAllocate

Returns the previous memory-allocation function before the call to this function.


#### - pfnOldFree

Returns the previous memory-releasing function before the call to this function.


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
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>



<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a>



<a href="https://msdn.microsoft.com/f6b6db72-c9af-44d1-9f84-26aaaa17691c">RpcSmSetClientAllocFree</a>
 

 

