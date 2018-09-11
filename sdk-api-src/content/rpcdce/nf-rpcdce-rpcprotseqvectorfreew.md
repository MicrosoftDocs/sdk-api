---
UID: NF:rpcdce.RpcProtseqVectorFreeW
title: RpcProtseqVectorFreeW function
author: windows-sdk-content
description: The RpcProtseqVectorFree function frees the protocol sequences contained in the vector and the vector itself.
old-location: rpc\rpcprotseqvectorfree.htm
tech.root: Rpc
ms.assetid: 6f399600-0534-44cc-b179-d3bc7bee091d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcProtseqVectorFree, RpcProtseqVectorFree function [RPC], RpcProtseqVectorFreeA, RpcProtseqVectorFreeW, _rpc_rpcprotseqvectorfree, rpc.rpcprotseqvectorfree, rpcdce/RpcProtseqVectorFree, rpcdce/RpcProtseqVectorFreeA, rpcdce/RpcProtseqVectorFreeW
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
req.unicode-ansi: RpcProtseqVectorFreeW (Unicode) and RpcProtseqVectorFreeA (ANSI)
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
 - RpcProtseqVectorFree
 - RpcProtseqVectorFreeA
 - RpcProtseqVectorFreeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcProtseqVectorFreeW function


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server calls 
<b>RpcProtseqVectorFree</b> to release the memory used to store a vector of protocol sequences and the individual protocol sequences. 
<b>RpcProtseqVectorFree</b> sets the <i>ProtSeqVector</i> parameter to a null value.

For a list of Microsoft RPC supported protocol sequences, see 
<a href="https://msdn.microsoft.com/5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305">String Binding</a>.

A server obtains a vector of protocol sequences by calling 
<a href="https://msdn.microsoft.com/7390e30a-9e29-417e-8d21-a045f1888036">RpcNetworkInqProtseqs</a>.

<div class="alert"><b>Note</b>  <b>RpcProtseqVectorFree</b> is available for server and client applications using Microsoft RPC, but is more common and convenient for server applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7390e30a-9e29-417e-8d21-a045f1888036">RpcNetworkInqProtseqs</a>
 

 

