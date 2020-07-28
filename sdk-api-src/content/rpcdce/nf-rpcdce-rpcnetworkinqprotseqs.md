---
UID: NF:rpcdce.RpcNetworkInqProtseqs
title: RpcNetworkInqProtseqs function (rpcdce.h)
description: The RpcNetworkInqProtseqs function returns all protocol sequences supported by both the RPC run-time library and the operating system.
helpviewer_keywords: ["RpcNetworkInqProtseqs","RpcNetworkInqProtseqs function [RPC]","RpcNetworkInqProtseqsA","RpcNetworkInqProtseqsW","_rpc_rpcnetworkinqprotseqs","rpc.rpcnetworkinqprotseqs","rpcdce/RpcNetworkInqProtseqs","rpcdce/RpcNetworkInqProtseqsA","rpcdce/RpcNetworkInqProtseqsW"]
old-location: rpc\rpcnetworkinqprotseqs.htm
tech.root: Rpc
ms.assetid: 7390e30a-9e29-417e-8d21-a045f1888036
ms.date: 12/05/2018
ms.keywords: RpcNetworkInqProtseqs, RpcNetworkInqProtseqs function [RPC], RpcNetworkInqProtseqsA, RpcNetworkInqProtseqsW, _rpc_rpcnetworkinqprotseqs, rpc.rpcnetworkinqprotseqs, rpcdce/RpcNetworkInqProtseqs, rpcdce/RpcNetworkInqProtseqsA, rpcdce/RpcNetworkInqProtseqsW
f1_keywords:
- rpcdce/RpcNetworkInqProtseqs
dev_langs:
- c++
req.header: rpcdce.h
req.include-header: Rpc.h
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
- RpcNetworkInqProtseqs
- RpcNetworkInqProtseqsA
- RpcNetworkInqProtseqsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcNetworkInqProtseqs function


## -description


The 
<b>RpcNetworkInqProtseqs</b> function returns all protocol sequences supported by both the RPC run-time library and the operating system. Client applications often use 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcnetworkisprotseqvalid">RpcNetworkIsProtseqValid</a>. For a list of Microsoft RPC's supported protocol sequences, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/string-binding">String Binding</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server application calls the 
<b>RpcNetworkInqProtseqs</b> function to obtain a vector containing the protocol sequences supported by both the RPC run-time library and the operating system. If there are no supported protocol sequences, this function returns the RPC_S_NO_PROTSEQS status code and a <i>ProtSeqVector</i> parameter value of <b>NULL</b>.

The server is responsible for calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcprotseqvectorfree">RpcProtseqVectorFree</a> function to release the memory used by the vector.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcnetworkisprotseqvalid">RpcNetworkIsProtseqValid</a>
 

 

