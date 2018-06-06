---
UID: NF:rpcndr.RpcSmSetClientAllocFree
title: RpcSmSetClientAllocFree function
author: windows-sdk-content
description: The RpcSmSetClientAllocFree function enables the memory allocation and release mechanisms used by the client stubs.
old-location: rpc\rpcsmsetclientallocfree.htm
old-project: Rpc
ms.assetid: f6b6db72-c9af-44d1-9f84-26aaaa17691c
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: RpcSmSetClientAllocFree, RpcSmSetClientAllocFree function [RPC], _rpc_rpcsmsetclientallocfree, rpc.rpcsmsetclientallocfree, rpcndr/RpcSmSetClientAllocFree
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcSmSetClientAllocFree
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcSmSetClientAllocFree function


## -description


The 
<b>RpcSmSetClientAllocFree</b> function enables the memory allocation and release mechanisms used by the client stubs.


## -parameters




### -param ClientAlloc

TBD


### -param ClientFree

TBD




#### - pfnAllocate

Function used to allocate memory.


#### - pfnFree

Function used to release memory and used with the function specified by <i>pfnAllocate</i>.


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
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



By overriding the default routines used by the client stub to manage memory, 
<b>RpcSmSetClientAllocFree</b> establishes the memory allocation and memory-freeing mechanisms. Note that the default routines are <a href="https://msdn.microsoft.com/8a49582a-9ae4-4f26-a172-bc8fe2aab65a">free</a> and <b>malloc</b>, unless the remote call occurs within manager code. In this case, the default memory–management functions are 
<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a> and 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>.




## -see-also




<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>



<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a>
 

 

