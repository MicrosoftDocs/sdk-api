---
UID: NF:rpcdce.RpcBindingSetOption
title: RpcBindingSetOption function (rpcdce.h)
description: The RpcBindingSetOption function enables client applications to specify message-queuing options on a binding handle.
helpviewer_keywords: ["RpcBindingSetOption","RpcBindingSetOption function [RPC]","_rpc_rpcbindingsetoption","rpc.rpcbindingsetoption","rpcdce/RpcBindingSetOption"]
old-location: rpc\rpcbindingsetoption.htm
tech.root: Rpc
ms.assetid: bc721fb0-2271-4658-995b-a41e8eefc5d5
ms.date: 12/05/2018
ms.keywords: RpcBindingSetOption, RpcBindingSetOption function [RPC], _rpc_rpcbindingsetoption, rpc.rpcbindingsetoption, rpcdce/RpcBindingSetOption
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
 - RpcBindingSetOption
 - rpcdce/RpcBindingSetOption
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
 - RpcBindingSetOption
---

# RpcBindingSetOption function


## -description

The 
<b>RpcBindingSetOption</b> function enables client applications to specify message-queuing options on a binding handle.

## -parameters

### -param hBinding

Server binding to modify.

### -param option

Binding property to modify. For a list of binding options and their possible values, see 
<a href="/windows/desktop/Rpc/binding-option-constants">Binding Option Constants</a>. See Remarks for information on the RPC Call time-out feature.

### -param optionValue

New value for the binding property. See Remarks.

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
The function is not supported for either the operating system or the transport. Note that calling 
<b>RpcBindingSetOption</b> on binding handles that use any protocol sequence other than <b>ncacn_*</b> will fail and return this value.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

RPC client processes use 
<b>RpcBindingSetOption</b> to control the delivery quality-of-service, call logging, and call lifetimes. Changing the binding-handle properties will affect all remote calls until the properties are changed by another call to 
<b>RpcBindingSetOption</b>. You can also call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a> to set security options for the binding handle.

<b>Windows XP:  </b>RPC Call Timeout feature:

Calling the 
<b>RpcBindingSetOption</b> function with <i>Option</i> set to RPC_C_OPT_CALL_TIMEOUT and <i>OptionValue</i> set to the time-out value (in milliseconds) enables developers to set an RPC-server time-out that prevents a thread from becoming captive to an unresponsive RPC server. This feature saves developers from explicitly canceling a call to an unresponsive RPC server. The timer monitoring for time-out is reset by the RPC client upon receipt of each packet. If the time-out expires without receiving a packet from the server, the RPC client returns RPC_S_CALL_CANCELLED. Note that the RPC server may still eventually execute a call, even though the client will discard the response.

Set <i>OptionValue</i> to INFINITE or zero for an infinite time-out. Do not change this option from another thread while a call is in progress. Do not attempt to retry a canceled call; doing so increases the burden on the already unresponsive server. The RPC call time-out feature is only useful for connection-oriented, synchronous RPC calls, such as those made on <b>ncacn_*</b> protocol sequences. For datagram, asynchronous, or local RPC calls, this option is ignored by the RPC run-time.

The RPC call time-out feature is useful in many situations, such as user interface updates that would otherwise wait for the busy RPC server to respond (leaving the user watching an hourglass), or when many RPC servers can service a request, thereby enabling clients to more quickly identify and bypass unresponsive servers.

## -see-also

<a href="/windows/desktop/Rpc/rpc-message-queuing">RPC Message
		  Queuing</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient">RpcBindingInqAuthClient</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption">RpcBindingInqOption</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a>



<a href="/windows/desktop/Midl/message">message</a>