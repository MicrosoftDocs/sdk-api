---
UID: NF:rpcdce.RpcRaiseException
title: RpcRaiseException function (rpcdce.h)
description: Use the RpcRaiseException function to raise an exception. The function does not return to the caller.
helpviewer_keywords: ["RpcRaiseException","RpcRaiseException function [RPC]","_rpc_rpcraiseexception","rpc.rpcraiseexception","rpcdce/RpcRaiseException"]
old-location: rpc\rpcraiseexception.htm
tech.root: Rpc
ms.assetid: 0bffc62e-a80e-4af1-a17a-ef4f00b9c4da
ms.date: 12/05/2018
ms.keywords: RpcRaiseException, RpcRaiseException function [RPC], _rpc_rpcraiseexception, rpc.rpcraiseexception, rpcdce/RpcRaiseException
req.header: rpcdce.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcRaiseException
 - rpcdce/RpcRaiseException
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
 - RpcRaiseException
---

# RpcRaiseException function


## -description

Use the 
<b>RpcRaiseException</b> function to raise an exception. The function does not return to the caller.

## -parameters

### -param exception

Exception code for the exception.

## -returns

This function does not return a value.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

<b>RpcRaiseException</b> raises an exception. The exception handler can then handle the exception. For more information about handling exceptions, see 
<a href="/windows/desktop/Rpc/making-rpc-function-calls">Making RPC Function Calls</a>.

## -see-also

<a href="/previous-versions/">RpcAbnormalTermination</a>



<a href="/windows/desktop/api/rpc/nf-rpc-rpcexcept">RpcExcept</a>



<a href="/previous-versions/aa375699(v=vs.80)">RpcFinally</a>