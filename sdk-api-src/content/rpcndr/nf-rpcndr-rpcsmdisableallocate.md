---
UID: NF:rpcndr.RpcSmDisableAllocate
title: RpcSmDisableAllocate function (rpcndr.h)
author: windows-sdk-content
description: The RpcSmDisableAllocate function frees resources and memory within the stub memory&#8211;management environment.
old-location: rpc\rpcsmdisableallocate.htm
tech.root: Rpc
ms.assetid: 229cab16-eabf-49d3-a61e-3c06e001d0ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RpcSmDisableAllocate, RpcSmDisableAllocate function [RPC], _rpc_rpcsmdisableallocate, rpc.rpcsmdisableallocate, rpcndr/RpcSmDisableAllocate
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
 - RpcSmDisableAllocate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcSmDisableAllocate function


## -description


The 
<b>RpcSmDisableAllocate</b> function frees resources and memory within the stub memory–management environment.


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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcSmDisableAllocate</b> function frees all the resources used by a call to 
<a href="https://msdn.microsoft.com/a0b144fc-873e-4884-b842-ac0eea84487b">RpcSmEnableAllocate</a>. It also releases memory allocated by a call to 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a> after the call to 
<b>RpcSmEnableAllocate</b> and marked for deletion by the 
<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a> function.

Note that 
<a href="https://msdn.microsoft.com/a0b144fc-873e-4884-b842-ac0eea84487b">RpcSmEnableAllocate</a> and 
<b>RpcSmDisableAllocate</b> must be used together as matching pairs.




## -see-also




<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>



<a href="https://msdn.microsoft.com/a0b144fc-873e-4884-b842-ac0eea84487b">RpcSmEnableAllocate</a>
 

 

