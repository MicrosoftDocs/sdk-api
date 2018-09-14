---
UID: NF:rpcndr.RpcSmDestroyClientContext
title: RpcSmDestroyClientContext function
author: windows-sdk-content
description: The RpcSmDestroyClientContext function reclaims the client memory resources for a context handle and makes the context handle NULL.
old-location: rpc\rpcsmdestroyclientcontext.htm
tech.root: rpc
ms.assetid: ae886740-09e9-46a1-aa62-5dbcf6abab36
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: RpcSmDestroyClientContext, RpcSmDestroyClientContext function [RPC], _rpc_rpcsmdestroyclientcontext, rpc.rpcsmdestroyclientcontext, rpcndr/RpcSmDestroyClientContext
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
 - RpcSmDestroyClientContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcSmDestroyClientContext function


## -description


The 
<b>RpcSmDestroyClientContext</b> function reclaims the client memory resources for a context handle and makes the context handle <b>NULL</b>.


## -parameters




### -param ContextHandle

Context handle that can no longer be used. The handle is set to <b>NULL</b> before <b>RpcSMDestroyClientContext</b> returns.


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
<dt><b>RPC_X_SS_CONTEXT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Client applications use 
<b>RpcSmDestroyClientContext</b> to reclaim resources from an inactive context handle. Applications can call 
<b>RpcSmDestroyClientContext</b> after a communications error makes the context handle unusable. The 
<b>RpcSmDestroyClientContext</b> function provides the same functionality as the 
<a href="https://msdn.microsoft.com/7c4fe939-eda9-45c3-84fb-491ac96e7c78">RpcSsDestroyClientContext</a> function.

This function does not invoke the server's context handle run-down process.

When 
<b>RpcSmDestroyClientContext</b> reclaims the memory resources, it also makes the context handle <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/a1f0408c-7739-4fca-b9b2-f045dad0c392">Using Context Handles</a>.




## -see-also




<a href="https://msdn.microsoft.com/7c4fe939-eda9-45c3-84fb-491ac96e7c78">RpcSsDestroyClientContext</a>
 

 

