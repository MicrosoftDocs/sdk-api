---
UID: NF:rpcnsi.RpcNsBindingLookupDone
title: RpcNsBindingLookupDone function (rpcnsi.h)
description: The RpcNsBindingLookupDone function signifies that a client has finished looking for compatible servers and deletes the lookup context.
helpviewer_keywords: ["RpcNsBindingLookupDone","RpcNsBindingLookupDone function [RPC]","_rpc_rpcnsbindinglookupdone","rpc.rpcnsbindinglookupdone","rpcnsi/RpcNsBindingLookupDone"]
old-location: rpc\rpcnsbindinglookupdone.htm
tech.root: Rpc
ms.assetid: bf272b29-8594-428a-947c-cc91ddfb4538
ms.date: 12/05/2018
ms.keywords: RpcNsBindingLookupDone, RpcNsBindingLookupDone function [RPC], _rpc_rpcnsbindinglookupdone, rpc.rpcnsbindinglookupdone, rpcnsi/RpcNsBindingLookupDone
req.header: rpcnsi.h
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
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNsBindingLookupDone
 - rpcnsi/RpcNsBindingLookupDone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsBindingLookupDone
---

# RpcNsBindingLookupDone function


## -description

The 
<b>RpcNsBindingLookupDone</b> function signifies that a client has finished looking for compatible servers and deletes the lookup context.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param LookupContext

Pointer to the name-service handle to free. The name-service handle <i>LookupContext</i> points to is created by calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a> function. 




An argument value of <b>NULL</b> is returned.

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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsBindingLookupDone</b> function frees a lookup context created by calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a> function.

Typically, a client application calls 
<b>RpcNsBindingLookupDone</b> after completing remote procedure calls to a server using a binding handle returned from the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a> function. However, a client application is responsible for calling 
<b>RpcNsBindingLookupDone</b> for each created lookup context, regardless of the status returned from the 
<b>RpcNsBindingLookupNext</b> function or the success in making remote procedure calls.

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>