---
UID: NF:rpcdce.RpcMgmtSetCancelTimeout
title: RpcMgmtSetCancelTimeout function (rpcdce.h)
description: The RpcMgmtSetCancelTimeout function sets the lower bound on the time to wait before timing out after forwarding a cancel.
helpviewer_keywords: ["RpcMgmtSetCancelTimeout","RpcMgmtSetCancelTimeout function [RPC]","_rpc_rpcmgmtsetcanceltimeout","rpc.rpcmgmtsetcanceltimeout","rpcdce/RpcMgmtSetCancelTimeout"]
old-location: rpc\rpcmgmtsetcanceltimeout.htm
tech.root: Rpc
ms.assetid: 0a616f5d-b30a-4cd3-9348-19f09f373c50
ms.date: 12/05/2018
ms.keywords: RpcMgmtSetCancelTimeout, RpcMgmtSetCancelTimeout function [RPC], _rpc_rpcmgmtsetcanceltimeout, rpc.rpcmgmtsetcanceltimeout, rpcdce/RpcMgmtSetCancelTimeout
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
 - RpcMgmtSetCancelTimeout
 - rpcdce/RpcMgmtSetCancelTimeout
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
 - RpcMgmtSetCancelTimeout
---

# RpcMgmtSetCancelTimeout function


## -description

The 
<b>RpcMgmtSetCancelTimeout</b> function sets the lower bound on the time to wait before timing out after forwarding a cancel.

## -parameters

### -param Timeout

Seconds to wait for a server to acknowledge a cancel command. To specify that a client waits an indefinite amount of time, supply the value RPC_C_CANCEL_INFINITE_TIMEOUT.

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
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
Called from an MS-DOS or Windows 3.<i>x</i> client.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls the 
<b>RpcMgmtSetCancelTimeout</b> function to reset the amount of time the run-time library waits for a server to acknowledge a cancel. The application specifies either to wait forever or to wait a specified length of time in seconds. If the value of <i>Seconds</i> is 0 (zero), the call is immediately abandoned upon a cancel command and control returns to the client application. The default value is RPC_C_CANCEL_INFINITE_TIMEOUT, which specifies waiting indefinitely for the call to complete.

The value for the cancel command time-out applies to all remote procedure calls made in the current thread. To change the time-out value, a multithreaded client must call this function in each thread of execution.