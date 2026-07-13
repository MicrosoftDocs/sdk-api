---
UID: NF:rpcdce.RpcProtseqVectorFreeA
title: RpcProtseqVectorFreeA function (rpcdce.h)
description: The RpcProtseqVectorFree function frees the protocol sequences contained in the vector and the vector itself. (RpcProtseqVectorFreeA)
helpviewer_keywords: ["RpcProtseqVectorFreeA", "rpcdce/RpcProtseqVectorFreeA"]
old-location: rpc\rpcprotseqvectorfree.htm
tech.root: Rpc
ms.assetid: 6f399600-0534-44cc-b179-d3bc7bee091d
ms.date: 12/05/2018
ms.keywords: RpcProtseqVectorFree, RpcProtseqVectorFree function [RPC], RpcProtseqVectorFreeA, RpcProtseqVectorFreeW, _rpc_rpcprotseqvectorfree, rpc.rpcprotseqvectorfree, rpcdce/RpcProtseqVectorFree, rpcdce/RpcProtseqVectorFreeA, rpcdce/RpcProtseqVectorFreeW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcProtseqVectorFreeW (Unicode) and RpcProtseqVectorFreeA (ANSI)
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
 - RpcProtseqVectorFreeA
 - rpcdce/RpcProtseqVectorFreeA
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
 - RpcProtseqVectorFree
 - RpcProtseqVectorFreeA
 - RpcProtseqVectorFreeW
---

# RpcProtseqVectorFreeA function


## -description

The 
<b>RpcProtseqVectorFree</b> function frees the protocol sequences contained in the vector and the vector itself.

## -parameters

### -param ProtseqVector

Pointer to a pointer to a vector of protocol sequences. On return, the pointer is set to NULL.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A server calls 
<b>RpcProtseqVectorFree</b> to release the memory used to store a vector of protocol sequences and the individual protocol sequences. 
<b>RpcProtseqVectorFree</b> sets the <i>ProtSeqVector</i> parameter to a null value.

For a list of Microsoft RPC supported protocol sequences, see 
<a href="/windows/desktop/Rpc/string-binding">String Binding</a>.

A server obtains a vector of protocol sequences by calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnetworkinqprotseqs">RpcNetworkInqProtseqs</a>.

<div class="alert"><b>Note</b>  <b>RpcProtseqVectorFree</b> is available for server and client applications using Microsoft RPC, but is more common and convenient for server applications.</div>
<div> </div>




> [!NOTE]
> The rpcdce.h header defines RpcProtseqVectorFree as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnetworkinqprotseqs">RpcNetworkInqProtseqs</a>
