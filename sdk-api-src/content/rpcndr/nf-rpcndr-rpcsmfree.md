---
UID: NF:rpcndr.RpcSmFree
title: RpcSmFree function
author: windows-sdk-content
description: The RpcSmFree function releases memory allocated by RpcSmAllocate.
old-location: rpc\rpcsmfree.htm
tech.root: Rpc
ms.assetid: d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcSmFree, RpcSmFree function [RPC], _rpc_rpcsmfree, rpc.rpcsmfree, rpcndr/RpcSmFree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - RpcSmFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcSmFree function


## -description


The 
<b>RpcSmFree</b> function releases memory allocated by 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>.


## -parameters




### -param NodeToFree

Pointer to memory allocated by 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a> or 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>.


## -returns



The function 
<b>RpcSmFree</b> returns the following value.

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



Applications use 
<b>RpcSmFree</b> to free memory allocated by 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>. In cases where the stub allocates the memory for the application, 
<b>RpcSmFree</b> can also be used to release memory. For more information, see 
<a href="https://msdn.microsoft.com/b56ccac1-84cb-4687-bdd2-21ee716b472a">Memory Management</a>.

To improve performance, the 
<b>RpcSmFree</b> function only marks memory for release. Memory is not actually released until your application calls the 
<a href="https://msdn.microsoft.com/229cab16-eabf-49d3-a61e-3c06e001d0ac">RpcSmDisableAllocate</a> function. To release memory immediately, invoke the 
<a href="https://msdn.microsoft.com/5e940e93-bdd4-48cc-b84e-654637699719">midl_user_free</a> function.

Note that the handle of the thread calling 
<b>RpcSmFree</b> must match the handle of the thread that allocated the memory by calling 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate.</a>. Use 
<a href="https://msdn.microsoft.com/5bf2c93c-8273-484b-a79f-821b2068692d">RpcSmGetThreadHandle</a> and 
<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a> to pass handles from thread to thread.




## -see-also




<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>



<a href="https://msdn.microsoft.com/5bf2c93c-8273-484b-a79f-821b2068692d">RpcSmGetThreadHandle</a>



<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a>



<a href="https://msdn.microsoft.com/">midl_user_allocate</a>
 

 

