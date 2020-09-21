---
UID: NF:midles.MesHandleFree
title: MesHandleFree function (midles.h)
description: The MesHandleFree function frees the memory allocated by the serialization handle.
helpviewer_keywords: ["MesHandleFree","MesHandleFree function [RPC]","_rpc_meshandlefree","midles/MesHandleFree","rpc.meshandlefree"]
old-location: rpc\meshandlefree.htm
tech.root: Rpc
ms.assetid: d4a4ac59-56fb-4693-9007-f358105f82f0
ms.date: 12/05/2018
ms.keywords: MesHandleFree, MesHandleFree function [RPC], _rpc_meshandlefree, midles/MesHandleFree, rpc.meshandlefree
req.header: midles.h
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
 - MesHandleFree
 - midles/MesHandleFree
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
 - MesHandleFree
---

# MesHandleFree function


## -description

The 
<b>MesHandleFree</b> function frees the memory allocated by the serialization handle.

## -parameters

### -param Handle

Handle to be freed.

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

The 
<b>MesHandleFree</b> routine is used by applications to free the resources of the handle after encoding or decoding data.

## -see-also

<a href="/windows/desktop/api/midles/nf-midles-mesdecodebufferhandlecreate">MesDecodeBufferHandleCreate</a>



<a href="/windows/desktop/api/midles/nf-midles-mesencodedynbufferhandlecreate">MesEncodeDynBufferHandleCreate</a>



<a href="/windows/desktop/api/midles/nf-midles-mesencodefixedbufferhandlecreate">MesEncodeFixedBufferHandleCreate</a>



<a href="/windows/desktop/api/midles/nf-midles-mesencodeincrementalhandlecreate">MesEncodeIncrementalHandleCreate</a>