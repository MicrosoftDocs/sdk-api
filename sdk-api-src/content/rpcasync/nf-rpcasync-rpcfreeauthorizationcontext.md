---
UID: NF:rpcasync.RpcFreeAuthorizationContext
title: RpcFreeAuthorizationContext function (rpcasync.h)
description: The RpcFreeAuthorizationContext function frees an Authz context obtained by a previous call to the RpcGetAuthorizationContextForClient function.
helpviewer_keywords: ["RpcFreeAuthorizationContext","RpcFreeAuthorizationContext function [RPC]","_rpc_rpcfreeauthorizationcontext","rpc.rpcfreeauthorizationcontext","rpcasync/RpcFreeAuthorizationContext"]
old-location: rpc\rpcfreeauthorizationcontext.htm
tech.root: Rpc
ms.assetid: ad6117e1-3244-42dd-b513-d5b2c28e8e10
ms.date: 12/05/2018
ms.keywords: RpcFreeAuthorizationContext, RpcFreeAuthorizationContext function [RPC], _rpc_rpcfreeauthorizationcontext, rpc.rpcfreeauthorizationcontext, rpcasync/RpcFreeAuthorizationContext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcFreeAuthorizationContext
 - rpcasync/RpcFreeAuthorizationContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcFreeAuthorizationContext
---

# RpcFreeAuthorizationContext function


## -description

The 
<b>RpcFreeAuthorizationContext</b> function frees an Authz context obtained by a previous call to the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient">RpcGetAuthorizationContextForClient</a> function.

## -parameters

### -param pAuthzClientContext [in]

Pointer to the previously obtained Authz client context to be freed.

## -returns

Successful completion returns RPC_S_OK. This function does not fail unless an invalid parameter is provided.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The <i>pAuthzClientContext</i> parameter is a pointer to the Authz context, not the context itself. To prevent accidental reuse of the Authz context freed by this function call, RPC run-time zeros out the context upon return.

## -see-also

<a href="/windows/desktop/SecAuthN/extended-error-information">Extended Error
		  Information</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient">RpcGetAuthorizationContextForClient</a>