---
UID: NF:rpcdce.RpcServerUseProtseqEpExA
title: RpcServerUseProtseqEpExA function (rpcdce.h)
description: The RpcServerUseProtseqEpEx function tells the RPC run-time library to use the specified protocol sequence combined with the specified endpoint for receiving remote procedure calls. (RpcServerUseProtseqEpExA)
helpviewer_keywords: ["RpcServerUseProtseqEpExA", "rpcdce/RpcServerUseProtseqEpExA"]
old-location: rpc\rpcserveruseprotseqepex.htm
tech.root: Rpc
ms.assetid: c5bc52c5-9799-4fab-89fa-a680639a229f
ms.date: 12/05/2018
ms.keywords: RpcServerUseProtseqEpEx, RpcServerUseProtseqEpEx function [RPC], RpcServerUseProtseqEpExA, RpcServerUseProtseqEpExW, _rpc_rpcserveruseprotseqepex, rpc.rpcserveruseprotseqepex, rpcdce/RpcServerUseProtseqEpEx, rpcdce/RpcServerUseProtseqEpExA, rpcdce/RpcServerUseProtseqEpExW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcServerUseProtseqEpExW (Unicode) and RpcServerUseProtseqEpExA (ANSI)
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
 - RpcServerUseProtseqEpExA
 - rpcdce/RpcServerUseProtseqEpExA
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
 - RpcServerUseProtseqEpEx
 - RpcServerUseProtseqEpExA
 - RpcServerUseProtseqEpExW
---

# RpcServerUseProtseqEpExA function


## -description

The 
<b>RpcServerUseProtseqEpEx</b> function tells the RPC run-time library to use the specified protocol sequence combined with the specified endpoint for receiving remote procedure calls.

## -parameters

### -param Protseq

Pointer to a string identifier of the protocol sequence to register with the RPC run-time library.

### -param MaxCalls

Backlog queue length for the <b>ncacn_ip_tcp</b> protocol sequence. All other protocol sequences ignore this parameter. Use RPC_C_PROTSEQ_MAX_REQS_DEFAULT to specify the default value. See Remarks.

### -param Endpoint

Pointer to the endpoint-address information to use in creating a binding for the protocol sequence specified by <i>Protseq</i>.

### -param SecurityDescriptor

Pointer to an optional parameter provided for the security subsystem. Used only for <b>ncacn_np</b> and <i>ncalrpc</i> protocol sequences. All other protocol sequences ignore this parameter. Using a security descriptor on the endpoint in order to make a server secure is not recommended. This parameter does not appear in the DCE specification for this API.

### -param Policy

Pointer to the 
<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_policy">RPC_POLICY</a> structure, which contains flags that set transport-specific attributes. In the case of the <b>ncadg_mq</b> transport, these flags specify the properties of the server process–receive queue. In the case of the <b>ncacn_ip_tcp</b> or <b>ncadg_ip_udp</b> transports, these flags restrict port allocation for dynamic ports and allow multihomed computers to selectively bind to network interface cards. 




The flag settings in the <b>Policy</b> field are effective only when the <b>ncacn_ip_tcp</b>, <b>ncadg_ip_udp</b>, or <b>ncadg_mq</b> protocol sequences are in use. For all other protocol sequences, the RPC run time ignores these values.

<div class="alert"><b>Note</b>  Portions of the policy associated with dynamic endpoints are ignored when the RpcServerUseProtseqEpEx function is called, since the port is specified in the endpoint itself.</div>
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
<dt><b>RPC_S_PROTSEQ_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The protocol sequence is not supported on this host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_RPC_PROTSEQ</b></dt>
</dl>
</td>
<td width="60%">
The protocol sequence is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ENDPOINT_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The endpoint format is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_DUPLICATE_ENDPOINT</b></dt>
</dl>
</td>
<td width="60%">
The endpoint is a duplicate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_SECURITY_DESC</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The parameters and effects of 
<b>RpcServerUseProtseqEpEx</b> subsume those of 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqep">RpcServerUseProtseqEp</a>. The difference is the <i>Policy</i> parameter, which allows you to set specific policies at the endpoints. Setting the <b>NICFlags</b> field of the 
<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_policy">RPC_POLICY</a> structure to zero makes this extended function equivalent to the original 
<b>RpcServerUseProtseqEp</b> when used with the <b>ncacn_ip_tcp</b> or <b>ncadg_ip_udp</b> transports.

A server application calls 
<b>RpcServerUseProtseqEpEx</b> to register one protocol sequence with the RPC run-time library. With each protocol sequence registration, 
<b>RpcServerUseProtseqEpEx</b> includes the specified endpoint-address information.

To receive remote procedure call requests, a server must register at least one protocol sequence with the RPC run-time library. A server application can call this routine many times to register additional protocol sequences and endpoints. For each protocol sequence registered by a server, the RPC run-time library creates one or more endpoints through which the server receives remote procedure call requests. The RPC run-time library creates different endpoints for each protocol sequence. However, each interface in the process is accessible through any endpoint. For more information, see Writing a Secure RPC Client or Server.

For <i>MaxCalls</i>, the value provided by the application is only a hint. The RPC run time or the Windows Sockets provider may override the value. For example, on Windows XP or Windows 2000 Professional, the value is limited to 5. Values greater than 5 are ignored and 5 is used instead. On Windows Server 2003 and Windows 2000 Server, the value will be honored.

Applications must be careful to pass reasonable values in <i>MaxCalls</i>. Large values on Server, Advanced Server, or Datacenter Server can cause a large amount of non-paged pool memory to be used. Using too small a value is also unfavorable, as it may result in TCP SYN packets being met by TCP RST from the server if the backlog queue gets exhausted. An application developer should balance memory footprint versus scalability requirements when determining the proper value for <i>MaxCalls</i>.

When the computer is configured to use selective binding, successful return does not guarantee that the server has created endpoints for all the network interfaces present on the computer.  The RPC run-time may not listen on some network interfaces depending on the selective binding settings.  In addition, if an interface has not yet received an IP address using DHCP, the RPC server does not listen on the network interface until a DHCP address is assigned to it.  A successful return implies that the server is listening on at least one network interface;  the full list of the binding handles over which remote procedure calls can be received can be obtained with a call to the RpcServerInqBindings function.



For more information, see 
<a href="/windows/desktop/Rpc/server-side-binding">Server-Side Binding</a>, 
<a href="/windows/desktop/Rpc/string-binding">String Binding</a>, 
<a href="/windows/desktop/Rpc/configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding">Configuring the Registry for Port Allocations and Selective Binding</a>, and 
<a href="/windows/desktop/Rpc/rpc-message-queuing">RPC Message Queuing</a> and the MIDL reference pages 
<a href="/windows/desktop/Midl/message">message</a> and 
<a href="/windows/desktop/Midl/ncadg-mq">ncadg_mq</a>.





> [!NOTE]
> The rpcdce.h header defines RpcServerUseProtseqEpEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_policy">RPC_POLICY</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsex">RpcServerUseAllProtseqsEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex">RpcServerUseAllProtseqsIfEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqex">RpcServerUseProtseqEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqifex">RpcServerUseProtseqIfEx</a>



Writing a Secure RPC Client or Server
