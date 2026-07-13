---
UID: NF:rpcdce.RpcNetworkIsProtseqValidA
title: RpcNetworkIsProtseqValidA function (rpcdce.h)
description: The RpcNetworkIsProtseqValid function tells whether the specified protocol sequence is supported by both the RPC run-time library and the operating system. Server applications often use RpcNetworkInqProtseqs. (RpcNetworkIsProtseqValidA)
helpviewer_keywords: ["RpcNetworkIsProtseqValidA", "rpcdce/RpcNetworkIsProtseqValidA"]
old-location: rpc\rpcnetworkisprotseqvalid.htm
tech.root: Rpc
ms.assetid: 72a28f64-2a66-4b61-96a9-80b8b9486151
ms.date: 12/05/2018
ms.keywords: RpcNetworkIsProtseqValid, RpcNetworkIsProtseqValid function [RPC], RpcNetworkIsProtseqValidA, RpcNetworkIsProtseqValidW, _rpc_rpcnetworkisprotseqvalid, rpc.rpcnetworkisprotseqvalid, rpcdce/RpcNetworkIsProtseqValid, rpcdce/RpcNetworkIsProtseqValidA, rpcdce/RpcNetworkIsProtseqValidW
req.header: rpcdce.h
req.include-header: Rpc.h
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNetworkIsProtseqValidA
 - rpcdce/RpcNetworkIsProtseqValidA
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
 - RpcNetworkIsProtseqValid
 - RpcNetworkIsProtseqValidA
 - RpcNetworkIsProtseqValidW
---

# RpcNetworkIsProtseqValidA function


## -description

The 
<b>RpcNetworkIsProtseqValid</b> function tells whether the specified protocol sequence is supported by both the RPC run-time library and the operating system. Server applications often use 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnetworkinqprotseqs">RpcNetworkInqProtseqs</a>.

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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls the 
<b>RpcNetworkIsProtseqValid</b> function to determine whether an individual protocol sequence is available for making remote procedure calls.

A protocol sequence is valid if both the RPC run-time library and the operating system support the specified protocols. For a list of Microsoft RPC's supported protocol sequences, see 
<a href="/windows/desktop/Rpc/string-binding">String Binding</a>. An application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnetworkinqprotseqs">RpcNetworkInqProtseqs</a> to see all of the supported protocol sequences.





> [!NOTE]
> The rpcdce.h header defines RpcNetworkIsProtseqValid as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnetworkinqprotseqs">RpcNetworkInqProtseqs</a>
