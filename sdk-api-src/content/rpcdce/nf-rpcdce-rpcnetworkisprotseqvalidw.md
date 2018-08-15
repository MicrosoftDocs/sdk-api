---
UID: NF:rpcdce.RpcNetworkIsProtseqValidW
title: RpcNetworkIsProtseqValidW function
author: windows-sdk-content
description: The RpcNetworkIsProtseqValid function tells whether the specified protocol sequence is supported by both the RPC run-time library and the operating system. Server applications often use RpcNetworkInqProtseqs.
old-location: rpc\rpcnetworkisprotseqvalid.htm
old-project: rpc
ms.assetid: 72a28f64-2a66-4b61-96a9-80b8b9486151
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RpcNetworkIsProtseqValid, RpcNetworkIsProtseqValid function [RPC], RpcNetworkIsProtseqValidA, RpcNetworkIsProtseqValidW, _rpc_rpcnetworkisprotseqvalid, rpc.rpcnetworkisprotseqvalid, rpcdce/RpcNetworkIsProtseqValid, rpcdce/RpcNetworkIsProtseqValidA, rpcdce/RpcNetworkIsProtseqValidW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNetworkIsProtseqValidW (Unicode) and RpcNetworkIsProtseqValidA (ANSI)
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
 - RpcNetworkIsProtseqValid
 - RpcNetworkIsProtseqValidA
 - RpcNetworkIsProtseqValidW
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcNetworkIsProtseqValidW function


## -description


The 
<b>RpcNetworkIsProtseqValid</b> function tells whether the specified protocol sequence is supported by both the RPC run-time library and the operating system. Server applications often use 
<a href="https://msdn.microsoft.com/7390e30a-9e29-417e-8d21-a045f1888036">RpcNetworkInqProtseqs</a>.


## -parameters




### -param Protseq

Pointer to a string identifier of the protocol sequence to be checked. 




If the <i>Protseq</i> parameter is not a valid protocol sequence string, 
<b>RpcNetworkIsProtseqValid</b> returns RPC_S_INVALID_RPC_PROTSEQ.


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
The call succeeded.; protocol sequence supported

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_PROTSEQ_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Protocol sequence not supported on this host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_RPC_PROTSEQ</b></dt>
</dl>
</td>
<td width="60%">
Invalid protocol sequence.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls the 
<b>RpcNetworkIsProtseqValid</b> function to determine whether an individual protocol sequence is available for making remote procedure calls.

A protocol sequence is valid if both the RPC run-time library and the operating system support the specified protocols. For a list of Microsoft RPC's supported protocol sequences, see 
<a href="https://msdn.microsoft.com/5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305">String Binding</a>. An application calls 
<a href="https://msdn.microsoft.com/7390e30a-9e29-417e-8d21-a045f1888036">RpcNetworkInqProtseqs</a> to see all of the supported protocol sequences.




## -see-also




<a href="https://msdn.microsoft.com/7390e30a-9e29-417e-8d21-a045f1888036">RpcNetworkInqProtseqs</a>
 

 

