---
UID: NF:rpcdce.RpcMgmtInqComTimeout
title: RpcMgmtInqComTimeout function (rpcdce.h)
description: The RpcMgmtInqComTimeout function returns the binding-communications time-out value in a binding handle.
helpviewer_keywords: ["RpcMgmtInqComTimeout","RpcMgmtInqComTimeout function [RPC]","_rpc_rpcmgmtinqcomtimeout","rpc.rpcmgmtinqcomtimeout","rpcdce/RpcMgmtInqComTimeout"]
old-location: rpc\rpcmgmtinqcomtimeout.htm
tech.root: Rpc
ms.assetid: e7bb9955-68a7-49fe-bcdb-2450518ffe0a
ms.date: 12/05/2018
ms.keywords: RpcMgmtInqComTimeout, RpcMgmtInqComTimeout function [RPC], _rpc_rpcmgmtinqcomtimeout, rpc.rpcmgmtinqcomtimeout, rpcdce/RpcMgmtInqComTimeout
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcMgmtInqComTimeout
 - rpcdce/RpcMgmtInqComTimeout
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
 - RpcMgmtInqComTimeout
---

# RpcMgmtInqComTimeout function


## -description

The 
<b>RpcMgmtInqComTimeout</b> function returns the binding-communications time-out value in a binding handle.

## -parameters

### -param Binding

Specifies a binding.

### -param Timeout

Returns a pointer to the time-out value from the <i>Binding</i> parameter.

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
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A client application calls 
<b>RpcMgmtInqComTimeout</b> to view the time-out value in a server binding handle. The time-out value specifies the relative amount of time that should be spent to wait for a response from the server before giving up. For a table of the time-out values, see 
<a href="/windows/desktop/Rpc/binding-time-out-constants">Binding Time-out Constants</a>. For more information on how the COM time-out operates, and when to use it, see 
<a href="/windows/desktop/Rpc/rpc-and-the-network">RPC and the Network</a>.

A client also calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout">RpcMgmtSetComTimeout</a> to change the time-out value.

## -see-also

<a href="/windows/desktop/Rpc/binding-time-out-constants">Binding
		  Time-out Constants</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtinqstats">RpcMgmtInqStats</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout">RpcMgmtSetComTimeout</a>