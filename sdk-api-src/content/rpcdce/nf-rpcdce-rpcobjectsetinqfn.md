---
UID: NF:rpcdce.RpcObjectSetInqFn
title: RpcObjectSetInqFn function (rpcdce.h)
description: The RpcObjectSetInqFn function registers an object-inquiry function. A null value turns off a previously registered object-inquiry function.
helpviewer_keywords: ["RpcObjectSetInqFn","RpcObjectSetInqFn function [RPC]","_rpc_rpcobjectsetinqfn","rpc.rpcobjectsetinqfn","rpcdce/RpcObjectSetInqFn"]
old-location: rpc\rpcobjectsetinqfn.htm
tech.root: Rpc
ms.assetid: 358d3ab3-df16-486b-aeac-56a0ffc78272
ms.date: 12/05/2018
ms.keywords: RpcObjectSetInqFn, RpcObjectSetInqFn function [RPC], _rpc_rpcobjectsetinqfn, rpc.rpcobjectsetinqfn, rpcdce/RpcObjectSetInqFn
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
 - RpcObjectSetInqFn
 - rpcdce/RpcObjectSetInqFn
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
 - RpcObjectSetInqFn
---

# RpcObjectSetInqFn function


## -description

The 
<b>RpcObjectSetInqFn</b> function registers an object-inquiry function. A null value turns off a previously registered object-inquiry function.

## -parameters

### -param InquiryFn

Object-type inquiry function. See 
<a href="/windows/desktop/api/rpcdce/nc-rpcdce-rpc_object_inq_fn">RPC_OBJECT_INQ_FN</a>. When an application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectinqtype">RpcObjectInqType</a> and the RPC run-time library finds that the specified object is not registered, the run-time library automatically calls 
<b>RpcObjectSetInqFn</b> to determine the object's type.

## -returns

This function returns the following value.

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

A server application calls 
<b>RpcObjectSetInqFn</b> to override the default mapping function that maps object UUIDs to type UUIDs, which determine an object's type. If an application privately maintains an object/type registration, the specified inquiry function returns the type UUID of an object.

The RPC run-time library automatically calls the inquiry function when the application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectinqtype">RpcObjectInqType</a> and the object of interest was not previously registered with 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectsettype">RpcObjectSetType</a>. The <i>TypeUuid</i> and <i>Status</i> values of the 
<a href="/windows/desktop/api/rpcdce/nc-rpcdce-rpc_object_inq_fn">RPC_OBJECT_INQ_FN</a> function are returned as the output from 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectinqtype">RpcObjectInqType</a>.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectinqtype">RpcObjectInqType</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectsettype">RpcObjectSetType</a>