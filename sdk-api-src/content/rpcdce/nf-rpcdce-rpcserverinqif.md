---
UID: NF:rpcdce.RpcServerInqIf
title: RpcServerInqIf function (rpcdce.h)
description: The RpcServerInqIf function returns the manager entry-point vector (EPV) registered for an interface.
helpviewer_keywords: ["RpcServerInqIf","RpcServerInqIf function [RPC]","_rpc_rpcserverinqif","rpc.rpcserverinqif","rpcdce/RpcServerInqIf"]
old-location: rpc\rpcserverinqif.htm
tech.root: Rpc
ms.assetid: 4c5f86a5-7867-4d5a-a255-5c0c57c7fe0a
ms.date: 12/05/2018
ms.keywords: RpcServerInqIf, RpcServerInqIf function [RPC], _rpc_rpcserverinqif, rpc.rpcserverinqif, rpcdce/RpcServerInqIf
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
 - RpcServerInqIf
 - rpcdce/RpcServerInqIf
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
 - RpcServerInqIf
---

# RpcServerInqIf function


## -description

The 
<b>RpcServerInqIf</b> function returns the manager entry-point vector (EPV) registered for an interface.

## -parameters

### -param IfSpec

Interface whose manager EPV is returned.

### -param MgrTypeUuid

Pointer to the manager type UUID whose manager EPV is returned. 




Specifying a parameter value of <b>NULL</b> (or a nil UUID) signifies to return the manager EPV registered with <i>IfSpec</i> and the nil manager type UUID.

### -param MgrEpv

Returns a pointer to the manager EPV for the requested interface.

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
<dt><b>RPC_S_UNKNOWN_IF</b></dt>
</dl>
</td>
<td width="60%">
The interface is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNKNOWN_MGR_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The manager type is unknown.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A server application calls the 
<b>RpcServerInqIf</b> function to determine the manager EPV for a registered interface and manager type UUID.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a>