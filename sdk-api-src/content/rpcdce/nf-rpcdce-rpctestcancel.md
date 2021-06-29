---
UID: NF:rpcdce.RpcTestCancel
title: RpcTestCancel function (rpcdce.h)
description: The RpcTestCancel function checks for a cancel indication.
helpviewer_keywords: ["RpcTestCancel","RpcTestCancel function [RPC]","_rpc_rpctestcancel","rpc.rpctestcancel","rpcdce/RpcTestCancel"]
old-location: rpc\rpctestcancel.htm
tech.root: Rpc
ms.assetid: 1fd3b84d-ea45-4267-ac30-e4e2cf037c92
ms.date: 12/05/2018
ms.keywords: RpcTestCancel, RpcTestCancel function [RPC], _rpc_rpctestcancel, rpc.rpctestcancel, rpcdce/RpcTestCancel
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
 - RpcTestCancel
 - rpcdce/RpcTestCancel
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
 - RpcTestCancel
---

# RpcTestCancel function


## -description

The 
<b>RpcTestCancel</b> function checks for a cancel indication.



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
The call has been canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other values</b></dt>
</dl>
</td>
<td width="60%">
The call has not been canceled.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>
It is not unusual for the 
<b>RpcTestCancel</b> function to return the value ERROR_ACCESS_DENIED. This indicates that the remote procedure call has not been canceled.

## -remarks

An application server stub calls 
<b>RpcTestCancel</b> to determine whether a call has been canceled. If the call has been canceled, RPC_S_OK is returned; otherwise, another value is returned.

This function should be called periodically by the server stub so that it can respond to cancels in a timely fashion. If the function returns RPC_S_OK, the stub should clean up its data structures and return to the client.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcservertestcancel">RpcServerTestCancel</a>
