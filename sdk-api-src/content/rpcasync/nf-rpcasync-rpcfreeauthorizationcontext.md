---
UID: NF:rpcasync.RpcFreeAuthorizationContext
title: RpcFreeAuthorizationContext function
author: windows-sdk-content
description: The RpcFreeAuthorizationContext function frees an Authz context obtained by a previous call to the RpcGetAuthorizationContextForClient function.
old-location: rpc\rpcfreeauthorizationcontext.htm
tech.root: Rpc
ms.assetid: ad6117e1-3244-42dd-b513-d5b2c28e8e10
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RpcFreeAuthorizationContext, RpcFreeAuthorizationContext function [RPC], _rpc_rpcfreeauthorizationcontext, rpc.rpcfreeauthorizationcontext, rpcasync/RpcFreeAuthorizationContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - RpcFreeAuthorizationContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcFreeAuthorizationContext function


## -description


The 
<b>RpcFreeAuthorizationContext</b> function frees an Authz context obtained by a previous call to the 
<a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a> function.


## -parameters




### -param pAuthzClientContext [in]

Pointer to the previously obtained Authz client context to be freed.


## -returns



Successful completion returns RPC_S_OK. This function does not fail unless an invalid parameter is provided.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The <i>pAuthzClientContext</i> parameter is a pointer to the Authz context, not the context itself. To prevent accidental reuse of the Authz context freed by this function call, RPC run-time zeros out the context upon return.




## -see-also




<a href="https://msdn.microsoft.com/a15c61f0-03cc-462f-b5c1-8e7f062e9523">Extended Error
		  Information</a>



<a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a>
 

 

