---
UID: NF:rpcndr.RpcSsAllocate
title: RpcSsAllocate function
author: windows-driver-content
description: The RpcSsAllocate function allocates memory within the RPC stub memory-management function, and returns a pointer to the allocated memory or NULL.
old-location: rpc\rpcssallocate.htm
old-project: Rpc
ms.assetid: d1c1af46-63c5-4e50-abfb-c4f251972427
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: RpcSsAllocate, RpcSsAllocate function [RPC], _rpc_rpcssallocate, rpc.rpcssallocate, rpcndr/RpcSsAllocate
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
-	RpcSsAllocate
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcSsAllocate function


## -description


The 
<b>RpcSsAllocate</b> function allocates memory within the RPC stub memory-management function, and returns a pointer to the allocated memory or <b>NULL</b>.


## -parameters




### -param Size

Size of memory to allocate, in bytes.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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



The 
<b>RpcSsAllocate</b> function allows an application to allocate memory within the RPC stub memory–management function. Prior to calling 
<b>RpcSsAllocate</b>, the memory-management environment must already be established. For memory management called within the stub, the stub itself usually establishes the necessary environment. For more information, see 
<a href="https://msdn.microsoft.com/b56ccac1-84cb-4687-bdd2-21ee716b472a">Memory Management</a>. When using 
<b>RpcSsAllocate</b> to allocate memory not called from the stub, the application must call 
<a href="https://msdn.microsoft.com/18060ed2-2250-47c7-8579-238edea44c66">RpcSsEnableAllocate</a> to establish the required memory-management environment.

The 
<b>RpcSsAllocate</b> routine returns a pointer to the allocated memory, if the call was successful. Otherwise, it raises an exception.

When the stub establishes the memory management, it frees any memory allocated by 
<b>RpcSsAllocate</b>. The application can free such memory before returning to the calling stub by calling 
<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a>.

By contrast, when the application establishes the memory management, it must free any allocated memory. It does so by calling either 
<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a> or 
<a href="https://msdn.microsoft.com/08121380-ff75-4f18-aae4-fdd01e1dfa8b">RpcSsDisableAllocate</a>.

To manage the same memory within the stub memory–management environment, multiple threads can call 
<b>RpcSsAllocate</b> and 
<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a>. In this case, the threads must share the same stub memory management–thread handle. Applications pass thread handles from thread-to-thread by calling 
<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a> and 
<a href="https://msdn.microsoft.com/8984e253-ea78-4ca2-bf24-83100a0ac79d">RPCSsSetThreadHandle</a>.

<div class="alert"><b>Note</b>  The 
<b>RpcSsAllocate</b> routine raises exceptions, unlike 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>, which returns the error code.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>



<a href="https://msdn.microsoft.com/08121380-ff75-4f18-aae4-fdd01e1dfa8b">RpcSsDisableAllocate</a>



<a href="https://msdn.microsoft.com/18060ed2-2250-47c7-8579-238edea44c66">RpcSsEnableAllocate</a>



<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a>



<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a>



<a href="https://msdn.microsoft.com/8984e253-ea78-4ca2-bf24-83100a0ac79d">RpcSsSetThreadHandle</a>
 

 

