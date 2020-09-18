---
UID: NF:rpcdce.RpcServerUseAllProtseqsEx
title: RpcServerUseAllProtseqsEx function (rpcdce.h)
description: The RpcServerUseAllProtseqsEx function tells the RPC run-time library to use all supported protocol sequences for receiving remote procedure calls.
helpviewer_keywords: ["RpcServerUseAllProtseqsEx","RpcServerUseAllProtseqsEx function [RPC]","_rpc_rpcserveruseallprotseqsex","rpc.rpcserveruseallprotseqsex","rpcdce/RpcServerUseAllProtseqsEx"]
old-location: rpc\rpcserveruseallprotseqsex.htm
tech.root: Rpc
ms.assetid: 4fc2ccbe-1b01-4157-b3e7-2c61397d78f7
ms.date: 12/05/2018
ms.keywords: RpcServerUseAllProtseqsEx, RpcServerUseAllProtseqsEx function [RPC], _rpc_rpcserveruseallprotseqsex, rpc.rpcserveruseallprotseqsex, rpcdce/RpcServerUseAllProtseqsEx
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
 - RpcServerUseAllProtseqsEx
 - rpcdce/RpcServerUseAllProtseqsEx
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
 - RpcServerUseAllProtseqsEx
---

# RpcServerUseAllProtseqsEx function


## -description

The 
<b>RpcServerUseAllProtseqsEx</b> function tells the RPC run-time library to use all supported protocol sequences for receiving remote procedure calls.

## -parameters

### -param MaxCalls

Backlog queue length for the <a href="/windows/desktop/Midl/ncacn-ip-tcp">ncacn_ip_tcp</a> protocol sequence. All other protocol sequences ignore this parameter. Use RPC_C_PROTSEQ_MAX_REQS_DEFAULT to specify the default value. See Remarks.

### -param SecurityDescriptor

Pointer to an optional parameter provided for the security subsystem. Used only for <a href="/windows/desktop/Midl/ncacn-np">ncacn_np</a> and <a href="/windows/desktop/Midl/ncalrpc">ncalrpc</a> protocol sequences. All other protocol sequences ignore this parameter. Using a security descriptor on the endpoint in order to make a server secure is not recommended. This parameter does not appear in the DCE specification for this API.

### -param Policy

Pointer to the 
<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_policy">RPC_POLICY</a> structure, which allows you to override the default policies for dynamic port allocation and binding to network interface cards (NICs) on multihomed computers (computers with multiple network cards).

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
<dt><b>RPC_S_NO_PROTSEQS</b></dt>
</dl>
</td>
<td width="60%">
There are no supported protocol sequences.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Sufficient memory is not available.

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

<div class="alert"><b>Note</b>  Listening on all supported protocol sequences is not recommended, because it causes the server to listen on all protocol sequences, including non-mainstream protocol sequences.  It is recommended that servers listen on <a href="/windows/desktop/Rpc/use-mainstream-protocol-sequences">mainstream</a> protocol sequences only.</div>
<div> </div>
The parameters and effects of 
<b>RpcServerUseAllProtseqsEx</b> subsume those of 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>. The difference is the <i>Policy</i> parameter, which allows you to restrict port allocation for dynamic ports and allows multihomed machines to selectively bind to specified NICs.

Setting the <b>NICFlags</b> field of the 
<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_policy">RPC_POLICY</a> structure to zero makes this extended API functionally equivalent to the original 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>, and the server will bind to NICs based on the settings in the system registry. For information on how the registry settings define the available Internet and intranet ports, see 
<a href="/windows/desktop/Rpc/configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding">Configuring the Registry for Port Allocations and Selective Binding</a>.

<div class="alert"><b>Note</b>  The flag settings in the <i>Policy</i> field are effective only when the 
<a href="/windows/desktop/Midl/ncacn-ip-tcp">ncacn_ip_tcp</a> or
<a href="/windows/desktop/Midl/ncadg-ip-udp">ncadg_ip_udp</a> protocol sequence is in use. For all other protocol sequences, the RPC run-time ignores these values.</div>
<div> </div>
A server application calls 
<b>RpcServerUseAllProtseqsEx</b> to register all supported protocol sequences with the RPC run-time library. To receive remote procedure calls, a server must register at least one protocol sequence with the RPC run-time library.

For each protocol sequence registered by a server, the RPC run-time library creates one or more endpoints through which the server receives remote procedure call requests. The RPC run-time library creates different endpoints for each protocol sequence. The endpoint name is generated by the RPC run time or the operating system. For example, for <a href="/windows/desktop/Midl/ncacn-ip-tcp">ncacn_ip_tcp</a>, the port number is dynamically determined by the RPC run time, depending on availability and registry settings.

<div class="alert"><b>Note</b>  Using the 
<b>RpcServerUseAllProtseqsEx</b> function does not cause the server to listen on the following protocol sequences:<ul>
<li>
<a href="/windows/desktop/Midl/ncacn-nb-nb">ncacn_nb_nb</a>
</li>
<li>
<a href="/windows/desktop/Midl/ncacn-nb-tcp">ncacn_nb_tcp</a>
</li>
<li>
<a href="/windows/desktop/Midl/ncacn-nb-ipx">ncacn_nb_ipx</a>
</li>
<li>
<a href="/windows/desktop/Midl/ncadg-mq">ncadg_mq</a>
</li>
<li>
<a href="/windows/desktop/Midl/ncacn-at-dsp">ncacn_at_dsp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/">ncacn_http</a>
</li>
</ul>
</div>
<div> </div>
<div class="alert"><b>Note</b>  To listen on any of those protocol sequences, each sequence must be selected individually.</div>
<div> </div>
For <i>MaxCalls</i>, the value provided by the application is only a hint. The RPC run time or the Windows Sockets provider may override the value. For example, on Windows XP or Windows 2000 Professional, the value is limited to 5. Values greater than 5 are ignored and 5 is used instead. On Windows Server 2003 and Windows 2000 Server, the value will be honored.

Applications must be careful to pass reasonable values in <i>MaxCalls</i>. Large values on Server, Advanced Server, or Datacenter Server can cause a large amount of non-paged pool memory to be used. Using too small a value is also unfavorable, as it may result in TCP SYN packets being met by TCP RST from the server if the backlog queue gets exhausted. An application developer should balance memory footprint versus scalability requirements when determining the proper value for <i>MaxCalls</i>.

When the computer is configured to use selective binding, successful return does not guarantee that the server has created endpoints for all the network interfaces present on the computer.  The RPC run-time may not listen on some network interfaces depending on the selective binding settings.  In addition, if an interface has not yet received an IP address using DHCP, the RPC server does not listen on the network interface until a DHCP address is assigned to it.  A successful return implies that the server is listening on at least one network interface;  the full list of the binding handles over which remote procedure calls can be received can be obtained with a call to the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a> function.



To selectively register protocol sequences, a server calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqex">RpcServerUseProtseqEx</a>, 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqifex">RpcServerUseProtseqIfEx</a>, or 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex">RpcServerUseProtseqEpEx</a>. See 
<a href="/windows/desktop/Rpc/server-side-binding">Server-Side Binding</a> for a description of the routines that a server will typically call after registering protocol sequences.

## -see-also

<a href="/windows/desktop/Rpc/configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding">Configuring the Registry for Port Allocations
		  and Selective Binding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex">RpcServerUseAllProtseqsIfEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex">RpcServerUseProtseqEpEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqex">RpcServerUseProtseqEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqifex">RpcServerUseProtseqIfEx</a>