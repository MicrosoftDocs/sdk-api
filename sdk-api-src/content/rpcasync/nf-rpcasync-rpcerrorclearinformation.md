---
UID: NF:rpcasync.RpcErrorClearInformation
title: RpcErrorClearInformation function (rpcasync.h)
description: The RpcErrorClearInformation function clears all extended error information on the current thread.
helpviewer_keywords: ["RpcErrorClearInformation","RpcErrorClearInformation function [RPC]","_rpc_rpcerrorclearinformation","rpc.rpcerrorclearinformation","rpcasync/RpcErrorClearInformation"]
old-location: rpc\rpcerrorclearinformation.htm
tech.root: Rpc
ms.assetid: ff96904c-285d-4d39-af3b-bf295c29e62f
ms.date: 12/05/2018
ms.keywords: RpcErrorClearInformation, RpcErrorClearInformation function [RPC], _rpc_rpcerrorclearinformation, rpc.rpcerrorclearinformation, rpcasync/RpcErrorClearInformation
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - RpcErrorClearInformation
 - rpcasync/RpcErrorClearInformation
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
 - RpcErrorClearInformation
---

# RpcErrorClearInformation function


## -description

The 
<b>RpcErrorClearInformation</b> function clears all extended error information on the current thread.



## -returns

This function has no return values.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The RPC Runtime usually handles the clearing of extended error information. In only two cases should callers use 
<b>RpcErrorClearInformation</b>:

<ul>
<li>If the calling component adds records to the thread using the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerroraddrecord">RpcErrorAddRecord</a> function, then decides it has not encountered a fatal error and continues processing the original, or the error is not connected to the records is has added. In this case, the calling component needs to clear the error information from the thread to prevent the propagation of potentially misleading error information.</li>
<li>If the calling component attempts multiple retries of an operation that returns extended error information. When an RPC call starts, the RPC Runtime clears any extended error information on the thread. However, if the calling component calls 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerroraddrecord">RpcErrorAddRecord</a> in a loop with many iterations, it may want to clear the error information, as the extended error information accumulates over time and can exhaust available memory.</li>
</ul>

## -see-also

<a href="/windows/desktop/Rpc/obtaining-extended-rpc-error-information">Obtaining Extended RPC Error Information</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerroraddrecord">RpcErrorAddRecord</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnextrecord">RpcErrorGetNextRecord</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorstartenumeration">RpcErrorStartEnumeration</a>
