---
UID: NF:rpcdce.RpcIfInqId
title: RpcIfInqId function (rpcdce.h)
description: The RpcIfInqId function returns the interface-identification part of an interface specification.
helpviewer_keywords: ["RpcIfInqId","RpcIfInqId function [RPC]","_rpc_rpcifinqid","rpc.rpcifinqid","rpcdce/RpcIfInqId"]
old-location: rpc\rpcifinqid.htm
tech.root: Rpc
ms.assetid: 1b91e88c-b242-472f-b719-60f96599cb67
ms.date: 12/05/2018
ms.keywords: RpcIfInqId, RpcIfInqId function [RPC], _rpc_rpcifinqid, rpc.rpcifinqid, rpcdce/RpcIfInqId
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
 - RpcIfInqId
 - rpcdce/RpcIfInqId
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
 - RpcIfInqId
---

# RpcIfInqId function


## -description

The 
<b>RpcIfInqId</b> function returns the interface-identification part of an interface specification.

## -parameters

### -param RpcIfHandle

Stub-generated structure specifying the interface to query.

### -param RpcIfId

Returns a pointer to the interface identification. The application provides memory for the returned data.

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

An application calls the 
<b>RpcIfInqId</b> function to obtain a copy of the interface identification from the provided interface specification.

The returned interface identification consists of the interface UUID and interface version numbers (major and minor) specified in the <i>IfSpec</i> parameter from the IDL file.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqif">RpcServerInqIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a>