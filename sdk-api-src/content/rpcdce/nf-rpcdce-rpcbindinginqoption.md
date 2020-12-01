---
UID: NF:rpcdce.RpcBindingInqOption
title: RpcBindingInqOption function (rpcdce.h)
description: RPC client processes use RpcBindingInqOption to determine current values of the binding options for a given binding handle.
helpviewer_keywords: ["RpcBindingInqOption","RpcBindingInqOption function [RPC]","_rpc_rpcbindinginqoption","rpc.rpcbindinginqoption","rpcdce/RpcBindingInqOption"]
old-location: rpc\rpcbindinginqoption.htm
tech.root: Rpc
ms.assetid: f148c827-d18a-41f2-834a-f6b77b331bcc
ms.date: 12/05/2018
ms.keywords: RpcBindingInqOption, RpcBindingInqOption function [RPC], _rpc_rpcbindinginqoption, rpc.rpcbindinginqoption, rpcdce/RpcBindingInqOption
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
 - RpcBindingInqOption
 - rpcdce/RpcBindingInqOption
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
 - RpcBindingInqOption
---

# RpcBindingInqOption function


## -description

RPC client processes use 
<b>RpcBindingInqOption</b> to determine current values of the binding options for a given binding handle.

## -parameters

### -param hBinding

Server binding about which to determine binding-option values.

### -param option

Binding handle property to inquire about.

### -param pOptionValue

Memory location to place the value for the specified <i>Option</i>

<div class="alert"><b>Note</b>  For a list of binding options and their possible values, see 
<a href="/windows/desktop/Rpc/binding-option-constants">Binding Option Constants</a>.</div>
<div> </div>

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
The function is not supported for either the operating system or the transport.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

Client processes call 
<b>RpcBindingInqOption</b> to determine the current settings of the binding handle options. To inquire about authentication settings clients call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient">RpcBindingInqAuthClient</a> function. .

## -see-also

<a href="/windows/desktop/Rpc/rpc-message-queuing">RPC Message
		  Queuing</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient">RpcBindingInqAuthClient</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption">RpcBindingSetOption</a>



<a href="/windows/desktop/Midl/message">message</a>