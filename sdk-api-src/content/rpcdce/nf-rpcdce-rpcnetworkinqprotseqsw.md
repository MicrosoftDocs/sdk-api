---
UID: NF:rpcdce.RpcNetworkInqProtseqsW
title: RpcNetworkInqProtseqsW function
author: windows-sdk-content
description: The RpcNetworkInqProtseqs function returns all protocol sequences supported by both the RPC run-time library and the operating system.
old-location: rpc\rpcnetworkinqprotseqs.htm
old-project: Rpc
ms.assetid: 7390e30a-9e29-417e-8d21-a045f1888036
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcNetworkInqProtseqs, RpcNetworkInqProtseqs function [RPC], RpcNetworkInqProtseqsA, RpcNetworkInqProtseqsW, _rpc_rpcnetworkinqprotseqs, rpc.rpcnetworkinqprotseqs, rpcdce/RpcNetworkInqProtseqs, rpcdce/RpcNetworkInqProtseqsA, rpcdce/RpcNetworkInqProtseqsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNetworkInqProtseqsW (Unicode) and RpcNetworkInqProtseqsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcNetworkInqProtseqs
 - RpcNetworkInqProtseqsA
 - RpcNetworkInqProtseqsW
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcNetworkInqProtseqsW function


## -description


The 
<b>RpcNetworkInqProtseqs</b> function returns all protocol sequences supported by both the RPC run-time library and the operating system. Client applications often use 
<a href="https://msdn.microsoft.com/72a28f64-2a66-4b61-96a9-80b8b9486151">RpcNetworkIsProtseqValid</a>. For a list of Microsoft RPC's supported protocol sequences, see 
<a href="https://msdn.microsoft.com/5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305">String Binding</a>.


## -parameters




### -param ProtseqVector

Returns a pointer to a pointer to a protocol sequence vector.


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
No supported protocol sequences.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server application calls the 
<b>RpcNetworkInqProtseqs</b> function to obtain a vector containing the protocol sequences supported by both the RPC run-time library and the operating system. If there are no supported protocol sequences, this function returns the RPC_S_NO_PROTSEQS status code and a <i>ProtSeqVector</i> parameter value of <b>NULL</b>.

The server is responsible for calling the 
<a href="https://msdn.microsoft.com/6f399600-0534-44cc-b179-d3bc7bee091d">RpcProtseqVectorFree</a> function to release the memory used by the vector.




## -see-also




<a href="https://msdn.microsoft.com/72a28f64-2a66-4b61-96a9-80b8b9486151">RpcNetworkIsProtseqValid</a>
 

 

