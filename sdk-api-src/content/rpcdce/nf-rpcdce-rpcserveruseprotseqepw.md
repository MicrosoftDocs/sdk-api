---
UID: NF:rpcdce.RpcServerUseProtseqEpW
title: RpcServerUseProtseqEpW function (rpcdce.h)
description: The RpcServerUseProtseqEpW (Unicode) function (rpcdce.h) tells the RPC run-time library to use the specified protocol sequence and endpoint for receiving remote procedure calls. 
helpviewer_keywords: ["RpcServerUseProtseqEp", "RpcServerUseProtseqEp function [RPC]", "RpcServerUseProtseqEpW", "_rpc_rpcserveruseprotseqep", "rpc.rpcserveruseprotseqep", "rpcdce/RpcServerUseProtseqEp", "rpcdce/RpcServerUseProtseqEpW"]
old-location: rpc\rpcserveruseprotseqep.htm
tech.root: Rpc
ms.assetid: 1914a90a-6dee-4517-9de1-d332124eb0a4
ms.date: 08/15/2022
ms.keywords: RpcServerUseProtseqEp, RpcServerUseProtseqEp function [RPC], RpcServerUseProtseqEpA, RpcServerUseProtseqEpW, _rpc_rpcserveruseprotseqep, rpc.rpcserveruseprotseqep, rpcdce/RpcServerUseProtseqEp, rpcdce/RpcServerUseProtseqEpA, rpcdce/RpcServerUseProtseqEpW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcServerUseProtseqEpW (Unicode) and RpcServerUseProtseqEpA (ANSI)
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
 - RpcServerUseProtseqEpW
 - rpcdce/RpcServerUseProtseqEpW
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
 - RpcServerUseProtseqEp
 - RpcServerUseProtseqEpA
 - RpcServerUseProtseqEpW
---

# RpcServerUseProtseqEpW function


## -description

The 
<b>RpcServerUseProtseqEp</b> function tells the RPC run-time library to use the specified protocol sequence combined with the specified endpoint for receiving remote procedure calls.

## -parameters

### -param Protseq

Pointer to a string identifier of the protocol sequence to register with the RPC run-time library.

### -param MaxCalls

Backlog queue length for the <b>ncacn_ip_tcp</b> protocol sequence. All other protocol sequences ignore this parameter. Use RPC_C_PROTSEQ_MAX_REQS_DEFAULT to specify the default value. See Remarks.

### -param Endpoint

Pointer to the endpoint-address information to use in creating a binding for the protocol sequence specified in the <i>Protseq</i> parameter.

### -param SecurityDescriptor

Pointer to an optional parameter provided for the security subsystem. Used only for <b>ncacn_np</b> and <b>ncalrpc</b> protocol sequences. All other protocol sequences ignore this parameter. Using a security descriptor on the endpoint in order to make a server secure is not recommended. This parameter does not appear in the DCE specification for this API.

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

A server application calls 
<b>RpcServerUseProtseqEp</b> to register one protocol sequence with the RPC run-time library. With each protocol sequence registration, 
<b>RpcServerUseProtseqEp</b> includes the specified endpoint-address information.

To receive remote procedure call requests, a server must register at least one protocol sequence with the RPC run-time library. A server application can call this routine multiple times to register additional protocol sequences and endpoints. For each protocol sequence registered by a server, the RPC run-time library creates one or more endpoints through which the server receives remote procedure call requests. The RPC run-time library creates different endpoints for each protocol sequence. However, each interface in the process is accessible through any endpoint. For more information, see Writing a Secure RPC Client or Server.

For <i>MaxCalls</i>, the value provided by the application is only a hint. The RPC run time or the Windows Sockets provider may override the value. For example, on Windows XP or Windows 2000 Professional, the value is limited to 5. Values greater than 5 are ignored and 5 is used instead. On Windows Server 2003 and Windows 2000 Server, the value will be honored.

Applications must be careful to pass reasonable values in <i>MaxCalls</i>. Large values on Server, Advanced Server, or Datacenter Server can cause a large amount of non-paged pool memory to be used. Using too small a value is also unfavorable, as it may result in TCP SYN packets being met by TCP RST from the server if the backlog queue gets exhausted. An application developer should balance memory footprint versus scalability requirements when determining the proper value for <i>MaxCalls</i>.

When the computer is configured to use selective binding, successful return does not guarantee that the server has created endpoints for all the network interfaces present on the computer.  The RPC run-time may not listen on some network interfaces depending on the selective binding settings.  In addition, if an interface has not yet received an IP address using DHCP, the RPC server does not listen on the network interface until a DHCP address is assigned to it.  A successful return implies that the server is listening on at least one network interface;  the full list of the binding handles over which remote procedure calls can be received can be obtained with a call to the RpcServerInqBindings function.



For more information, see 
<a href="/windows/desktop/Rpc/server-side-binding">Server-Side Binding</a> and 
<a href="/windows/desktop/Rpc/string-binding">String Binding</a>.





> [!NOTE]
> The rpcdce.h header defines RpcServerUseProtseqEp as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingvectorfree">RpcBindingVectorFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverlisten">RpcServerListen</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif">RpcServerRegisterIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqs">RpcServerUseAllProtseqs</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif">RpcServerUseAllProtseqsIf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseq">RpcServerUseProtseq</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif">RpcServerUseProtseqIf</a>



Writing a Secure RPC Client or Server
