---
UID: NF:rpcdce.RpcStringFree
title: RpcStringFree function (rpcdce.h)
description: The RpcStringFree function (rpcdce.h) frees a character string allocated by the RPC run-time library.
helpviewer_keywords: ["RpcStringFree","RpcStringFree function [RPC]","RpcStringFreeA","RpcStringFreeW","_rpc_rpcstringfree","rpc.rpcstringfree","rpcdce/RpcStringFree","rpcdce/RpcStringFreeA","rpcdce/RpcStringFreeW"]
old-location: rpc\rpcstringfree.htm
tech.root: Rpc
ms.assetid: 07226282-1091-4479-adc8-b2f604c645e7
ms.date: 08/15/2022
ms.keywords: RpcStringFree, RpcStringFree function [RPC], RpcStringFreeA, RpcStringFreeW, _rpc_rpcstringfree, rpc.rpcstringfree, rpcdce/RpcStringFree, rpcdce/RpcStringFreeA, rpcdce/RpcStringFreeW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcStringFreeW (Unicode) and RpcStringFreeA (ANSI)
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
 - RpcStringFree
 - rpcdce/RpcStringFree
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
 - RpcStringFree
 - RpcStringFreeA
 - RpcStringFreeW
---

# RpcStringFree function


## -description

The 
<b>RpcStringFree</b> function frees a character string allocated by the RPC run-time library.

## -parameters

### -param String

Pointer to a pointer to the character string to free.

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

An application is responsible for calling 
<b>RpcStringFree</b> once for each character string allocated and returned by calls to other RPC run-time library routines.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingtostringbinding">RpcBindingToStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcnsbindinginqentryname">RpcNsBindingInqEntryName</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringbindingparse">RpcStringBindingParse</a>
