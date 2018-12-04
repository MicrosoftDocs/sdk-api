---
UID: NF:rpcdce.RpcServerUseAllProtseqsEx
title: RpcServerUseAllProtseqsEx function
author: windows-sdk-content
description: The RpcServerUseAllProtseqsEx function tells the RPC run-time library to use all supported protocol sequences for receiving remote procedure calls.
old-location: rpc\rpcserveruseallprotseqsex.htm
tech.root: rpc
ms.assetid: 4fc2ccbe-1b01-4157-b3e7-2c61397d78f7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RpcServerUseAllProtseqsEx, RpcServerUseAllProtseqsEx function [RPC], _rpc_rpcserveruseallprotseqsex, rpc.rpcserveruseallprotseqsex, rpcdce/RpcServerUseAllProtseqsEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcServerUseAllProtseqsEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcServerUseAllProtseqsEx function


## -description


The 
<b>RpcServerUseAllProtseqsEx</b> function tells the RPC run-time library to use all supported protocol sequences for receiving remote procedure calls.


## -parameters




### -param MaxCalls

Backlog queue length for the <a href="https://msdn.microsoft.com/8142c667-9a5f-4066-a36d-1bb5ce551d21">ncacn_ip_tcp</a> protocol sequence. All other protocol sequences ignore this parameter. Use RPC_C_PROTSEQ_MAX_REQS_DEFAULT to specify the default value. See Remarks.


### -param SecurityDescriptor

Pointer to an optional parameter provided for the security subsystem. Used only for <a href="https://msdn.microsoft.com/02961bb8-faf0-42e5-b134-dd2983e6d146">ncacn_np</a> and <a href="https://msdn.microsoft.com/0009f794-5c14-4484-9023-cb20c7030dc5">ncalrpc</a> protocol sequences. All other protocol sequences ignore this parameter. Using a security descriptor on the endpoint in order to make a server secure is not recommended. This parameter does not appear in the DCE specification for this API.


### -param Policy

Pointer to the 
<a href="https://msdn.microsoft.com/2647d75d-09b5-48b2-9a79-4d1f95cb094b">RPC_POLICY</a> structure, which allows you to override the default policies for dynamic port allocation and binding to network interface cards (NICs) on multihomed computers (computers with multiple network cards).


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<div class="alert"><b>Note</b>  Listening on all supported protocol sequences is not recommended, because it causes the server to listen on all protocol sequences, including non-mainstream protocol sequences.  It is recommended that servers listen on <a href="https://msdn.microsoft.com/60692247-bc39-448d-b92a-1879c08df8f1">mainstream</a> protocol sequences only.</div>
<div> </div>
The parameters and effects of 
<b>RpcServerUseAllProtseqsEx</b> subsume those of 
<a href="https://msdn.microsoft.com/e7379656-d6b7-4e5f-9251-7b112a40c6d5">RpcServerUseAllProtseqs</a>. The difference is the <i>Policy</i> parameter, which allows you to restrict port allocation for dynamic ports and allows multihomed machines to selectively bind to specified NICs.

Setting the <b>NICFlags</b> field of the 
<a href="https://msdn.microsoft.com/2647d75d-09b5-48b2-9a79-4d1f95cb094b">RPC_POLICY</a> structure to zero makes this extended API functionally equivalent to the original 
<a href="https://msdn.microsoft.com/e7379656-d6b7-4e5f-9251-7b112a40c6d5">RpcServerUseAllProtseqs</a>, and the server will bind to NICs based on the settings in the system registry. For information on how the registry settings define the available Internet and intranet ports, see 
<a href="https://msdn.microsoft.com/a33b51e7-2ded-46bd-aadb-27cbd99e1029">Configuring the Registry for Port Allocations and Selective Binding</a>.

<div class="alert"><b>Note</b>  The flag settings in the <i>Policy</i> field are effective only when the 
<a href="https://msdn.microsoft.com/8142c667-9a5f-4066-a36d-1bb5ce551d21">ncacn_ip_tcp</a> or
<a href="https://msdn.microsoft.com/c9133fcc-6dc2-49da-9c6f-5ce3c51090d5">ncadg_ip_udp</a> protocol sequence is in use. For all other protocol sequences, the RPC run-time ignores these values.</div>
<div> </div>
A server application calls 
<b>RpcServerUseAllProtseqsEx</b> to register all supported protocol sequences with the RPC run-time library. To receive remote procedure calls, a server must register at least one protocol sequence with the RPC run-time library.

For each protocol sequence registered by a server, the RPC run-time library creates one or more endpoints through which the server receives remote procedure call requests. The RPC run-time library creates different endpoints for each protocol sequence. The endpoint name is generated by the RPC run time or the operating system. For example, for <a href="https://msdn.microsoft.com/8142c667-9a5f-4066-a36d-1bb5ce551d21">ncacn_ip_tcp</a>, the port number is dynamically determined by the RPC run time, depending on availability and registry settings.

<div class="alert"><b>Note</b>  Using the 
<b>RpcServerUseAllProtseqsEx</b> function does not cause the server to listen on the following protocol sequences:<ul>
<li>
<a href="https://msdn.microsoft.com/8bab2784-44ba-4356-85c1-5bd17e75d6a8">ncacn_nb_nb</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3633842c-d1f5-46d9-866e-e54f31415ea5">ncacn_nb_tcp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/641471d4-eba4-4d4a-a3fe-1e40b3751e38">ncacn_nb_ipx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/">ncadg_mq</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3165e4f6-8869-4eff-af65-53e85f78a949">ncacn_at_dsp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/92d2b44c-2eab-4474-826b-ccafd26db124">ncacn_http</a>
</li>
</ul>
</div>
<div> </div>
<div class="alert"><b>Note</b>  To listen on any of those protocol sequences, each sequence must be selected individually.</div>
<div> </div>
For <i>MaxCalls</i>, the value provided by the application is only a hint. The RPC run time or the Windows Sockets provider may override the value. For example, on Windows XP or Windows 2000 Professional, the value is limited to 5. Values greater than 5 are ignored and 5 is used instead. On Windows Server 2003 and Windows 2000 Server, the value will be honored.

Applications must be careful to pass reasonable values in <i>MaxCalls</i>. Large values on Server, Advanced Server, or Datacenter Server can cause a large amount of non-paged pool memory to be used. Using too small a value is also unfavorable, as it may result in TCP SYN packets being met by TCP RST from the server if the backlog queue gets exhausted. An application developer should balance memory footprint versus scalability requirements when determining the proper value for <i>MaxCalls</i>.

When the computer is configured to use selective binding, successful return does not guarantee that the server has created endpoints for all the network interfaces present on the computer.  The RPC run-time may not listen on some network interfaces depending on the selective binding settings.  In addition, if an interface has not yet received an IP address using DHCP, the RPC server does not listen on the network interface until a DHCP address is assigned to it.  A successful return implies that the server is listening on at least one network interface;  the full list of the binding handles over which remote procedure calls can be received can be obtained with a call to the <a href="https://msdn.microsoft.com/96f081ab-6210-4ca0-a913-182477463981">RpcServerInqBindings</a> function.



To selectively register protocol sequences, a server calls 
<a href="https://msdn.microsoft.com/a8cedfe9-9c16-4c35-9cc4-5ccaa9e130a8">RpcServerUseProtseqEx</a>, 
<a href="https://msdn.microsoft.com/28238ff2-0ed0-4cb5-8117-b6c544d8c098">RpcServerUseProtseqIfEx</a>, or 
<a href="https://msdn.microsoft.com/c5bc52c5-9799-4fab-89fa-a680639a229f">RpcServerUseProtseqEpEx</a>. See 
<a href="https://msdn.microsoft.com/3c9e69e8-9745-4e62-9ddc-1bc04b4bef59">Server-Side Binding</a> for a description of the routines that a server will typically call after registering protocol sequences.




## -see-also




<a href="https://msdn.microsoft.com/a33b51e7-2ded-46bd-aadb-27cbd99e1029">Configuring the Registry for Port Allocations
		  and Selective Binding</a>



<a href="https://msdn.microsoft.com/118c931e-29ca-4ffb-aa32-24c6f4289cc8">RpcServerUseAllProtseqsIfEx</a>



<a href="https://msdn.microsoft.com/c5bc52c5-9799-4fab-89fa-a680639a229f">RpcServerUseProtseqEpEx</a>



<a href="https://msdn.microsoft.com/a8cedfe9-9c16-4c35-9cc4-5ccaa9e130a8">RpcServerUseProtseqEx</a>



<a href="https://msdn.microsoft.com/28238ff2-0ed0-4cb5-8117-b6c544d8c098">RpcServerUseProtseqIfEx</a>
 

 

