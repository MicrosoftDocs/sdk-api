---
UID: NC:rpcdce.RPC_AUTH_KEY_RETRIEVAL_FN
title: RPC_AUTH_KEY_RETRIEVAL_FN (rpcdce.h)
description: The RPC_AUTH_KEY_RETRIEVAL_FN function is a prototype for a function that specifies the address of a server-application-provided routine returning encryption keys.
helpviewer_keywords: ["RPC_AUTH_KEY_RETRIEVAL_FN","RPC_AUTH_KEY_RETRIEVAL_FN callback","RPC_AUTH_KEY_RETRIEVAL_FN callback function [RPC]","RpcAuthKeyRetrievalFn","_rpc_rpc_auth_key_retrieval_fn","rpc.rpc_auth_key_retrieval_fn","rpcdce/RPC_AUTH_KEY_RETRIEVAL_FN"]
old-location: rpc\rpc_auth_key_retrieval_fn.htm
tech.root: Rpc
ms.assetid: 643ce467-5df9-4b1a-a149-cf301865d47a
ms.date: 12/05/2018
ms.keywords: RPC_AUTH_KEY_RETRIEVAL_FN, RPC_AUTH_KEY_RETRIEVAL_FN callback, RPC_AUTH_KEY_RETRIEVAL_FN callback function [RPC], RpcAuthKeyRetrievalFn, _rpc_rpc_auth_key_retrieval_fn, rpc.rpc_auth_key_retrieval_fn, rpcdce/RPC_AUTH_KEY_RETRIEVAL_FN
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RPC_AUTH_KEY_RETRIEVAL_FN
 - rpcdce/RPC_AUTH_KEY_RETRIEVAL_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rpcdce.h
api_name:
 - RPC_AUTH_KEY_RETRIEVAL_FN
---

# RPC_AUTH_KEY_RETRIEVAL_FN callback function


## -description

The 
<i>RPC_AUTH_KEY_RETRIEVAL_FN</i> function is a prototype for a function that specifies the address of a server-application-provided routine returning encryption keys.

## -parameters

### -param Arg

Pointer to a user-defined argument to the user-supplied encryption key acquisition function. The RPC run-time library uses the <i>Arg</i> parameter supplied to 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo">RpcServerRegisterAuthInfo</a>.

### -param ServerPrincName

Pointer to the principal name to use for the server when authenticating remote procedure calls. The RPC run-time library uses the <i>ServerPrincName</i> parameter supplied to 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo">RpcServerRegisterAuthInfo</a>.

### -param KeyVer

Value that the RPC run-time library automatically provides for the key-version parameter. When the value is zero, the acquisition function must return the most recent key available.


#### - **Key

Pointer to a pointer to the authentication key returned by the user-supplied function.

### -param Status

Pointer to the status returned by the acquisition function when it is called by the RPC run-time library to authenticate the client RPC request. If the status is other than RPC_S_OK, the request fails and the run-time library returns the error status to the client application.

### -param Key

Pointer to a pointer to the authentication key returned by the user-supplied function.

## -remarks

An authorization key–retrieval function specifies the address of a server-application-provided routine returning encryption keys.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo">RpcServerRegisterAuthInfo</a>
