---
UID: NF:rpcndr.RpcSmAllocate
title: RpcSmAllocate function
author: windows-driver-content
description: The RpcSmAllocate function allocates memory within the RPC stub memory management function and returns a pointer to the allocated memory or NULL.
old-location: rpc\rpcsmallocate.htm
old-project: Rpc
ms.assetid: ca3373fa-8ea4-452e-b2a2-f30eb48fef9d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: RpcSmAllocate, RpcSmAllocate function [RPC], _rpc_rpcsmallocate, rpc.rpcsmallocate, rpcndr/RpcSmAllocate
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
-	RpcSmAllocate
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcSmAllocate function


## -description


The 
<b>RpcSmAllocate</b> function allocates memory within the RPC stub memory management function and returns a pointer to the allocated memory or <b>NULL</b>.


## -parameters




### -param Size

Size of memory to allocate, in bytes.


### -param pStatus

Pointer to the returned status.


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



The 
<b>RpcSmAllocate</b> routine allows an application to allocate memory within the RPC stub memory–management environment. Prior to calling 
<b>RpcSmAllocate</b>, the memory-management environment must already be established. For memory management called within the stub, the server stub itself may establish the necessary environment. For more information, see 
<a href="https://msdn.microsoft.com/a0b144fc-873e-4884-b842-ac0eea84487b">RpcSmEnableAllocate</a>. When using 
<b>RpcSmAllocate</b> to allocate memory not called from the stub, the application must call 
<b>RpcSmEnableAllocate</b> to establish the required memory-management environment.

The 
<b>RpcSmAllocate</b> routine returns a pointer to the allocated memory if the call is successful. Otherwise, a <b>NULL</b> is returned.

When the stub establishes the memory management, it frees any memory allocated by 
<b>RpcSmAllocate</b>. The application can free such memory before returning to the calling stub by calling 
<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a>.

By contrast, when the application establishes the memory management, it must free any memory allocated. It does so by calling either 
<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a> or 
<a href="https://msdn.microsoft.com/229cab16-eabf-49d3-a61e-3c06e001d0ac">RpcSmDisableAllocate</a>.

To manage the same memory within the stub memory–management environment, multiple threads can call 
<b>RpcSmAllocate</b> and 
<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a>. In this case, the threads must share the same stub memory management thread handle. Applications pass thread handles from thread to thread by calling 
<a href="https://msdn.microsoft.com/5bf2c93c-8273-484b-a79f-821b2068692d">RpcSmGetThreadHandle</a> and 
<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a>.

For more information, see 
<a href="https://msdn.microsoft.com/b56ccac1-84cb-4687-bdd2-21ee716b472a">Memory Management</a>.




## -see-also




<a href="https://msdn.microsoft.com/229cab16-eabf-49d3-a61e-3c06e001d0ac">RpcSmDisableAllocate</a>



<a href="https://msdn.microsoft.com/a0b144fc-873e-4884-b842-ac0eea84487b">RpcSmEnableAllocate</a>



<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a>



<a href="https://msdn.microsoft.com/5bf2c93c-8273-484b-a79f-821b2068692d">RpcSmGetThreadHandle</a>



<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a>
 

 

