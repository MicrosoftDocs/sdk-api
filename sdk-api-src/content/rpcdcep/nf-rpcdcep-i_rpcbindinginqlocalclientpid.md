---
UID: NF:rpcdcep.I_RpcBindingInqLocalClientPID
title: I_RpcBindingInqLocalClientPID function (rpcdcep.h)
description: Obtains a client process ID.
helpviewer_keywords: ["I_RpcBindingInqLocalClientPID","I_RpcBindingInqLocalClientPID function [RPC]","rpc.i_rpcbindinginqlocalclientpid","rpcdcep/I_RpcBindingInqLocalClientPID"]
old-location: rpc\i_rpcbindinginqlocalclientpid.htm
tech.root: Rpc
ms.assetid: af31dc1e-51b9-4789-a97f-d51ae34850cf
ms.date: 12/05/2018
ms.keywords: I_RpcBindingInqLocalClientPID, I_RpcBindingInqLocalClientPID function [RPC], rpc.i_rpcbindinginqlocalclientpid, rpcdcep/I_RpcBindingInqLocalClientPID
req.header: rpcdcep.h
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
 - I_RpcBindingInqLocalClientPID
 - rpcdcep/I_RpcBindingInqLocalClientPID
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
 - I_RpcBindingInqLocalClientPID
---

# I_RpcBindingInqLocalClientPID function


## -description

<p class="CCE_Message">[The <b>I_RpcBindingInqLocalClientPID</b> function is available for use in the operating systems specified in the Requirements section. Instead, call <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a>.]

The <b>I_RpcBindingInqLocalClientPID</b> function obtains a client process ID.

## -parameters

### -param Binding [in, optional]

<b>RPC_BINDING_HANDLE</b> that specifies the binding handle for an explicit RPC binding from the client to a server application.

### -param Pid [out]

Contains the process ID of the client that issued the call upon return.

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
The function call was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_CALL_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The current thread does not have an active RPC call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The RPC binding handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The client process ID is only returned in <i>ClientBinding</i> when the "ncalrpc" protocol sequence is used. Until the process terminates, the process ID value uniquely identifies it on the client. When the process terminates, the process ID can be used by new processes.