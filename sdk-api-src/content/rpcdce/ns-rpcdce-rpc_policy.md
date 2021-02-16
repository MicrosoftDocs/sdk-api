---
UID: NS:rpcdce._RPC_POLICY
title: RPC_POLICY (rpcdce.h)
description: The RPC_POLICY structure contains flags that determine binding on multihomed computers, and port allocations when using the ncacn_ip_tcp and ncadg_ip_udp protocols.
helpviewer_keywords: ["*PRPC_POLICY","0","PRPC_POLICY","PRPC_POLICY structure pointer [RPC]","RPC_C_BIND_TO_ALL_NICS","RPC_C_MQ_AUTHENTICATE","RPC_C_MQ_AUTHN_LEVEL_NONE","RPC_C_MQ_AUTHN_LEVEL_PKT_INTEGRITY","RPC_C_MQ_AUTHN_LEVEL_PKT_PRIVACY","RPC_C_MQ_CLEAR_ON_OPEN","RPC_C_MQ_ENCRYPT","RPC_C_MQ_PERMANENT","RPC_C_MQ_TEMPORARY","RPC_C_MQ_USE_EXISTING_SECURITY","RPC_C_USE_INTERNET_PORT","RPC_C_USE_INTRANET_PORT","RPC_POLICY","RPC_POLICY structure [RPC]","_rpc_rpc_policy","rpc.rpc_policy","rpcdce/PRPC_POLICY","rpcdce/RPC_POLICY"]
old-location: rpc\rpc_policy.htm
tech.root: Rpc
ms.assetid: 2647d75d-09b5-48b2-9a79-4d1f95cb094b
ms.date: 12/05/2018
ms.keywords: '*PRPC_POLICY, 0, PRPC_POLICY, PRPC_POLICY structure pointer [RPC], RPC_C_BIND_TO_ALL_NICS, RPC_C_MQ_AUTHENTICATE, RPC_C_MQ_AUTHN_LEVEL_NONE, RPC_C_MQ_AUTHN_LEVEL_PKT_INTEGRITY, RPC_C_MQ_AUTHN_LEVEL_PKT_PRIVACY, RPC_C_MQ_CLEAR_ON_OPEN, RPC_C_MQ_ENCRYPT, RPC_C_MQ_PERMANENT, RPC_C_MQ_TEMPORARY, RPC_C_MQ_USE_EXISTING_SECURITY, RPC_C_USE_INTERNET_PORT, RPC_C_USE_INTRANET_PORT, RPC_POLICY, RPC_POLICY structure [RPC], _rpc_rpc_policy, rpc.rpc_policy, rpcdce/PRPC_POLICY, rpcdce/RPC_POLICY'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_POLICY, *PRPC_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_POLICY
 - rpcdce/_RPC_POLICY
 - PRPC_POLICY
 - rpcdce/PRPC_POLICY
 - RPC_POLICY
 - rpcdce/RPC_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_POLICY
---

# RPC_POLICY structure


## -description

The 
<b>RPC_POLICY</b> structure contains flags that determine binding on multihomed computers, and port allocations when using the 
<a href="/windows/desktop/Midl/ncacn-ip-tcp">ncacn_ip_tcp</a> and 
<a href="/windows/desktop/Midl/ncadg-ip-udp">ncadg_ip_udp</a> protocols.

## -struct-fields

### -field Length

Size of the 
<b>RPC_POLICY</b> structure, in bytes. The <b>Length</b> member allows compatibility with future versions of this structure, which may contain additional fields. Always set the <b>Length</b> equal to <b>sizeof</b>(RPC_POLICY) when you initialize the 
<b>RPC_POLICY</b> structure in your code.

### -field EndpointFlags

Set of flags that determine the attributes of the port or ports where the server receives remote procedure calls. You can specify more than one flag (by using the bitwise OR operator) from the set of values for a given protocol sequence. The following table lists the possible values for the <b>EndpointFlags</b> member. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Specifies the system default.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_USE_INTERNET_PORT"></a><a id="rpc_c_use_internet_port"></a><dl>
<dt><b>RPC_C_USE_INTERNET_PORT</b></dt>
</dl>
</td>
<td width="60%">
Allocates the endpoint from one of the ports defined in the registry as "Internet Available." Valid only with 
<a href="/windows/desktop/Midl/ncacn-ip-tcp">ncacn_ip_tcp</a> and 
<a href="/windows/desktop/Midl/ncadg-ip-udp">ncadg_ip_udp</a> protocol sequences.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_USE_INTRANET_PORT"></a><a id="rpc_c_use_intranet_port"></a><dl>
<dt><b>RPC_C_USE_INTRANET_PORT</b></dt>
</dl>
</td>
<td width="60%">
Allocates the endpoint from one of the ports defined in the registry as "Intranet Available." Valid only with 
<a href="/windows/desktop/Midl/ncacn-ip-tcp">ncacn_ip_tcp</a> and 
<a href="/windows/desktop/Midl/ncadg-ip-udp">ncadg_ip_udp</a> protocol sequences.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_TEMPORARY"></a><a id="rpc_c_mq_temporary"></a><dl>
<dt><b>RPC_C_MQ_TEMPORARY</b></dt>
</dl>
</td>
<td width="60%">
The server process–receive queue will be deleted automatically when the RPC server exits. Any outstanding calls still in the queue will be lost. This is the default. Valid only with the 
<a href="/windows/desktop/Midl/ncadg-mq">ncadg_mq</a> protocol sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_PERMANENT"></a><a id="rpc_c_mq_permanent"></a><dl>
<dt><b>RPC_C_MQ_PERMANENT</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the server process–receive queue persists after the server process exits. The default is that the queue is deleted when the server process terminates. Valid only with ncadg_mq protocol sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_CLEAR_ON_OPEN"></a><a id="rpc_c_mq_clear_on_open"></a><dl>
<dt><b>RPC_C_MQ_CLEAR_ON_OPEN</b></dt>
</dl>
</td>
<td width="60%">
If the receive queue already exists because it was opened previously as a permanent queue, then clear any outstanding calls waiting in the queue. Valid only with the ncadg_mq protocol sequence only.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_USE_EXISTING_SECURITY"></a><a id="rpc_c_mq_use_existing_security"></a><dl>
<dt><b>RPC_C_MQ_USE_EXISTING_SECURITY</b></dt>
</dl>
</td>
<td width="60%">
If the receive queue already exists, then do not modify its existing settings for authentication or encryption. Valid only with the ncadg_mq protocol sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_AUTHENTICATE"></a><a id="rpc_c_mq_authenticate"></a><dl>
<dt><b>RPC_C_MQ_AUTHENTICATE</b></dt>
</dl>
</td>
<td width="60%">
The server process–receive queue accepts only authenticated calls from clients. The default is that both authenticated and unauthenticated calls are accepted. Valid only with ncadg_mq protocol sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_ENCRYPT"></a><a id="rpc_c_mq_encrypt"></a><dl>
<dt><b>RPC_C_MQ_ENCRYPT</b></dt>
</dl>
</td>
<td width="60%">
Calls to server are encrypted. The default is that both encrypted and unencrypted calls are accepted. Valid only with ncadg_mq protocol sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_AUTHN_LEVEL_NONE"></a><a id="rpc_c_mq_authn_level_none"></a><dl>
<dt><b>RPC_C_MQ_AUTHN_LEVEL_NONE</b></dt>
</dl>
</td>
<td width="60%">
The server's receive queue accepts all calls from clients. This is the default authentication level. Valid only with the 
<a href="/windows/desktop/Midl/ncadg-mq">ncadg_mq</a> protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_AUTHN_LEVEL_PKT_INTEGRITY"></a><a id="rpc_c_mq_authn_level_pkt_integrity"></a><dl>
<dt><b>RPC_C_MQ_AUTHN_LEVEL_PKT_INTEGRITY</b></dt>
</dl>
</td>
<td width="60%">
Sets the server's receive queue to only accept client calls that have authentication level RPC_C_AUTHN_LEVEL_PKT_INTEGRITY or RPC_C_AUTHN_LEVEL_PKT_PRIVACY. Valid only with the ncadg_mq protocol sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_AUTHN_LEVEL_PKT_PRIVACY"></a><a id="rpc_c_mq_authn_level_pkt_privacy"></a><dl>
<dt><b>RPC_C_MQ_AUTHN_LEVEL_PKT_PRIVACY</b></dt>
</dl>
</td>
<td width="60%">
Sets the server's receive queue to only accept client calls that have authentication level RPC_C_AUTHN_LEVEL_PKT_PRIVACY. Calls with a lower authentication level are ignored. Valid only with the ncadg_mq protocol sequence.

</td>
</tr>
</table>
 


<div> </div>


<div class="alert"><b>Note</b>  If the registry does not contain any of the keys that specify the default policies, then the <b>EndpointFlags</b> member will have no effect at run time. If a key is missing or contains an invalid value, then the entire configuration for that protocol (
<a href="/windows/desktop/Midl/ncacn-ip-tcp">ncacn_ip_tcp</a>, 
<a href="/windows/desktop/Midl/ncadg-ip-udp">ncadg_ip_udp</a> or 
<a href="/windows/desktop/Midl/ncadg-mq">ncadg_mq</a>) is marked as invalid and all calls to <b>RpcServerUseProtseq*</b> functions over that protocol will fail.</div>
<div> </div>

### -field NICFlags

Policy for binding to Network Interface Cards (NICs). The following table lists the possible values for the <b>NICFlags</b> member. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Binds to NICs on the basis of the registry settings. Always use this value when you are using the 
<b>RPC_POLICY</b> structure to define message-queue properties.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_BIND_TO_ALL_NICS"></a><a id="rpc_c_bind_to_all_nics"></a><dl>
<dt><b>RPC_C_BIND_TO_ALL_NICS</b></dt>
</dl>
</td>
<td width="60%">
Overrides the registry settings and binds to all NICs. If the Bind key is missing from the registry, then the <b>NICFlags</b> member will have no effect at run time. If the key contains an invalid value, then the entire configuration is marked as invalid and all calls to 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseq">RpcServerUseProtseq</a>* will fail.

</td>
</tr>
</table>

## -remarks

You can use the <b>RPC_Policy</b> structure to set policies for remote procedure calls at run time. These policies include:

<ul>
<li>Message queuing: Allows the server to specify message-queuing properties, such as security, quality of delivery, and the lifetime of the server-process queue. This policy is only effective for remote calls over the message-queuing transport (ncadg_mq).</li>
<li>Port allocation for dynamic ports: Specifies whether the endpoint registered by this application should go to the Internet-available or intranet-available port set.</li>
<li>Selective binding: Allows multihomed machines to bind selectively to NICs.</li>
</ul>
<div class="alert"><b>Note</b>  Port allocation and selective binding policies are effective only for remote calls over TCP (
<a href="/windows/desktop/Midl/ncacn-ip-tcp">ncacn_ip_tcp</a>) and UDP (
<a href="/windows/desktop/Midl/ncadg-ip-udp">ncadg_ip_udp</a>) connections. For more information, see 
<a href="/windows/desktop/Rpc/configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding">Configuring the Registry for Port Allocations and Selective Binding</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Rpc/configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding">Configuring the Registry for Port Allocations and Selective Binding</a>



<a href="/windows/desktop/Rpc/rpc-message-queuing">RPC Message Queuing</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsex">RpcServerUseAllProtseqsEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex">RpcServerUseAllProtseqsIfEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex">RpcServerUseProtseqEpEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqex">RpcServerUseProtseqEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqifex">RpcServerUseProtseqIfEx</a>