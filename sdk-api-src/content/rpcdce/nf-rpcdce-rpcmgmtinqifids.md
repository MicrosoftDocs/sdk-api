---
UID: NF:rpcdce.RpcMgmtInqIfIds
title: RpcMgmtInqIfIds function (rpcdce.h)
description: The RpcMgmtInqIfIds function returns a vector containing the identifiers of the interfaces offered by the server.
helpviewer_keywords: ["RpcMgmtInqIfIds","RpcMgmtInqIfIds function [RPC]","_rpc_rpcmgmtinqifids","rpc.rpcmgmtinqifids","rpcdce/RpcMgmtInqIfIds"]
old-location: rpc\rpcmgmtinqifids.htm
tech.root: Rpc
ms.assetid: f6d89f2c-ff51-44ab-9f8a-2f76cd3ac6db
ms.date: 12/05/2018
ms.keywords: RpcMgmtInqIfIds, RpcMgmtInqIfIds function [RPC], _rpc_rpcmgmtinqifids, rpc.rpcmgmtinqifids, rpcdce/RpcMgmtInqIfIds
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
 - RpcMgmtInqIfIds
 - rpcdce/RpcMgmtInqIfIds
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
 - RpcMgmtInqIfIds
---

# RpcMgmtInqIfIds function


## -description

The 
<b>RpcMgmtInqIfIds</b> function returns a vector containing the identifiers of the interfaces offered by the server.

## -parameters

### -param Binding

To receive interface identifiers about a remote application, specify a server binding handle for that application. To receive interface information about your own application, specify a value of <b>NULL</b>.

### -param IfIdVector

Returns the address of an interface identifier vector.

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

An application calls the 
<b>RpcMgmtInqIfIds</b> function to obtain a vector of interface identifiers about the specified server from the RPC run-time library.

The RPC run-time library allocates memory for the interface identifier vector. The application is responsible for calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifidvectorfree">RpcIfIdVectorFree</a> function to release the memory used by this vector.

The server must be listening for remote procedure calls for this function to succeed.  If the server is not listening, the function fails.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifidvectorfree">RpcIfIdVectorFree</a>