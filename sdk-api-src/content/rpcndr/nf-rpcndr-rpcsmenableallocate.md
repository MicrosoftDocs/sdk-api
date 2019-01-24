---
UID: NF:rpcndr.RpcSmEnableAllocate
title: RpcSmEnableAllocate function
author: windows-sdk-content
description: The RpcSmEnableAllocate function establishes the stub memory&#8211;management environment.
old-location: rpc\rpcsmenableallocate.htm
tech.root: Rpc
ms.assetid: a0b144fc-873e-4884-b842-ac0eea84487b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcSmEnableAllocate, RpcSmEnableAllocate function [RPC], _rpc_rpcsmenableallocate, rpc.rpcsmenableallocate, rpcndr/RpcSmEnableAllocate
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
 - RpcSmEnableAllocate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcSmEnableAllocate function


## -description


The 
<b>RpcSmEnableAllocate</b> function establishes the stub memory–management environment.


## -parameters






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



In cases where the stub memory management is not enabled by the server stub itself, applications call 
<b>RpcSmEnableAllocate</b> to establish the stub memory–management environment. This environment must be established prior to making a call to 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>. In OSF-compatibility (<b>/osf</b>) mode, for server manager code called from the stub, the memory-management environment may be established by the server stub itself by using pointer manipulation or the 
<a href="https://msdn.microsoft.com/3a232a82-f114-4d8c-8b71-cf8860c77db3">enable_allocate</a> attribute. In default (Microsoft-extended) mode, the environment is established only upon request by using the 
<a href="https://msdn.microsoft.com/3a232a82-f114-4d8c-8b71-cf8860c77db3">enable_allocate</a> attribute. Otherwise, call 
<b>RpcSmEnableAllocate</b> before calling 
<b>RpcSmAllocate</b>. For more information, see 
<a href="https://msdn.microsoft.com/b56ccac1-84cb-4687-bdd2-21ee716b472a">Memory Management</a>, 
<a href="https://msdn.microsoft.com/5bf2c93c-8273-484b-a79f-821b2068692d">RpcSmGetThreadHandle</a>, and 
<a href="https://msdn.microsoft.com/90bfd7f3-c95b-450b-8578-6e46d3ac7517">RpcSmSetThreadHandle</a>.




## -see-also




<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>



<a href="https://msdn.microsoft.com/229cab16-eabf-49d3-a61e-3c06e001d0ac">RpcSmDisableAllocate</a>
 

 

