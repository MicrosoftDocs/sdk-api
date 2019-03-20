---
UID: NS:rpcdce._RPC_POLICY
title: RPC_POLICY (rpcdce.h)
author: windows-sdk-content
description: The RPC_POLICY structure contains flags that determine binding on multihomed computers, and port allocations when using the ncacn_ip_tcp and ncadg_ip_udp protocols.
old-location: rpc\rpc_policy.htm
tech.root: Rpc
ms.assetid: 2647d75d-09b5-48b2-9a79-4d1f95cb094b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PRPC_POLICY, 0, PRPC_POLICY, PRPC_POLICY structure pointer [RPC], RPC_C_BIND_TO_ALL_NICS, RPC_C_MQ_AUTHENTICATE, RPC_C_MQ_AUTHN_LEVEL_NONE, RPC_C_MQ_AUTHN_LEVEL_PKT_INTEGRITY, RPC_C_MQ_AUTHN_LEVEL_PKT_PRIVACY, RPC_C_MQ_CLEAR_ON_OPEN, RPC_C_MQ_ENCRYPT, RPC_C_MQ_PERMANENT, RPC_C_MQ_TEMPORARY, RPC_C_MQ_USE_EXISTING_SECURITY, RPC_C_USE_INTERNET_PORT, RPC_C_USE_INTRANET_PORT, RPC_POLICY, RPC_POLICY structure [RPC], _rpc_rpc_policy, rpc.rpc_policy, rpcdce/PRPC_POLICY, rpcdce/RPC_POLICY"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_POLICY
product: Windows
targetos: Windows
req.typenames: RPC_POLICY, *PRPC_POLICY
req.redist: 
---

# RPC_POLICY structure


## -description


The 
<b>RPC_POLICY</b> structure contains flags that determine binding on multihomed computers, and port allocations when using the 
<a href="https://msdn.microsoft.com/8142c667-9a5f-4066-a36d-1bb5ce551d21">ncacn_ip_tcp</a> and 
<a href="https://msdn.microsoft.com/c9133fcc-6dc2-49da-9c6f-5ce3c51090d5">ncadg_ip_udp</a> protocols.


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
<a href="https://msdn.microsoft.com/8142c667-9a5f-4066-a36d-1bb5ce551d21">ncacn_ip_tcp</a> and 
<a href="https://msdn.microsoft.com/c9133fcc-6dc2-49da-9c6f-5ce3c51090d5">ncadg_ip_udp</a> protocol sequences.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_USE_INTRANET_PORT"></a><a id="rpc_c_use_intranet_port"></a><dl>
<dt><b>RPC_C_USE_INTRANET_PORT</b></dt>
</dl>
</td>
<td width="60%">
Allocates the endpoint from one of the ports defined in the registry as "Intranet Available." Valid only with 
<a href="https://msdn.microsoft.com/8142c667-9a5f-4066-a36d-1bb5ce551d21">ncacn_ip_tcp</a> and 
<a href="https://msdn.microsoft.com/c9133fcc-6dc2-49da-9c6f-5ce3c51090d5">ncadg_ip_udp</a> protocol sequences.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_MQ_TEMPORARY"></a><a id="rpc_c_mq_temporary"></a><dl>
<dt><b>RPC_C_MQ_TEMPORARY</b></dt>
</dl>
</td>
<td width="60%">
The server process–receive queue will be deleted automatically when the RPC server exits. Any outstanding calls still in the queue will be lost. This is the default. Valid only with the 
<a href="https://msdn.microsoft.com/">ncadg_mq</a> protocol sequence.

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
<a href="https://msdn.microsoft.com/">ncadg_mq</a> protocol.

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
<a href="https://msdn.microsoft.com/8142c667-9a5f-4066-a36d-1bb5ce551d21">ncacn_ip_tcp</a>, 
<a href="https://msdn.microsoft.com/c9133fcc-6dc2-49da-9c6f-5ce3c51090d5">ncadg_ip_udp</a> or 
<a href="https://msdn.microsoft.com/">ncadg_mq</a>) is marked as invalid and all calls to <b>RpcServerUseProtseq*</b> functions over that protocol will fail.</div>
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
<a href="https://msdn.microsoft.com/9b2c9cf0-fe96-4063-a893-f2793595af57">RpcServerUseProtseq</a>* will fail.

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
<a href="https://msdn.microsoft.com/8142c667-9a5f-4066-a36d-1bb5ce551d21">ncacn_ip_tcp</a>) and UDP (
<a href="https://msdn.microsoft.com/c9133fcc-6dc2-49da-9c6f-5ce3c51090d5">ncadg_ip_udp</a>) connections. For more information, see 
<a href="https://msdn.microsoft.com/a33b51e7-2ded-46bd-aadb-27cbd99e1029">Configuring the Registry for Port Allocations and Selective Binding</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a33b51e7-2ded-46bd-aadb-27cbd99e1029">Configuring the Registry for Port Allocations and Selective Binding</a>



<a href="https://msdn.microsoft.com/f1c8665b-3754-4c2e-b3ac-bba1f4b329e1">RPC Message Queuing</a>



<a href="https://msdn.microsoft.com/4fc2ccbe-1b01-4157-b3e7-2c61397d78f7">RpcServerUseAllProtseqsEx</a>



<a href="https://msdn.microsoft.com/118c931e-29ca-4ffb-aa32-24c6f4289cc8">RpcServerUseAllProtseqsIfEx</a>



<a href="https://msdn.microsoft.com/c5bc52c5-9799-4fab-89fa-a680639a229f">RpcServerUseProtseqEpEx</a>



<a href="https://msdn.microsoft.com/a8cedfe9-9c16-4c35-9cc4-5ccaa9e130a8">RpcServerUseProtseqEx</a>



<a href="https://msdn.microsoft.com/28238ff2-0ed0-4cb5-8117-b6c544d8c098">RpcServerUseProtseqIfEx</a>
 

 

