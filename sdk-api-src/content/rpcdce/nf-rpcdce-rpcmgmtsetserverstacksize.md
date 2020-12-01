---
UID: NF:rpcdce.RpcMgmtSetServerStackSize
title: RpcMgmtSetServerStackSize function (rpcdce.h)
description: The RpcMgmtSetServerStackSize function specifies the stack size for server threads created by the RPC run time.
helpviewer_keywords: ["RpcMgmtSetServerStackSize","RpcMgmtSetServerStackSize function [RPC]","_rpc_rpcmgmtsetserverstacksize","rpc.rpcmgmtsetserverstacksize","rpcdce/RpcMgmtSetServerStackSize"]
old-location: rpc\rpcmgmtsetserverstacksize.htm
tech.root: Rpc
ms.assetid: 5cf04ff5-d25b-42f5-a14e-2e73225765e9
ms.date: 12/05/2018
ms.keywords: RpcMgmtSetServerStackSize, RpcMgmtSetServerStackSize function [RPC], _rpc_rpcmgmtsetserverstacksize, rpc.rpcmgmtsetserverstacksize, rpcdce/RpcMgmtSetServerStackSize
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
 - RpcMgmtSetServerStackSize
 - rpcdce/RpcMgmtSetServerStackSize
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
 - RpcMgmtSetServerStackSize
---

# RpcMgmtSetServerStackSize function


## -description

The 
<b>RpcMgmtSetServerStackSize</b> function specifies the stack size for server threads created by the RPC run time.

## -parameters

### -param ThreadStackSize

Stack size allocated for each thread created by the RPC run time, in bytes. This value is applied to all threads created for the server, but not to threads already created. Select this value based on the stack requirements of the remote procedures offered by the server.

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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A server application calls the 
<b>RpcMgmtSetServerStackSize</b> function to specify the thread stack size to use when the RPC run-time library creates call threads for executing remote procedure calls.

Servers that know the stack requirements of all the manager functions in the interfaces it offers can call the 
<b>RpcMgmtSetServerStackSize</b> function to ensure that each call thread has the necessary stack size.

Calling 
<b>RpcMgmtSetServerStackSize</b> is optional. If a server does not call 
<b>RpcMgmtSetServerStackSize</b>, the default thread stack size from the executable image is used.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a>