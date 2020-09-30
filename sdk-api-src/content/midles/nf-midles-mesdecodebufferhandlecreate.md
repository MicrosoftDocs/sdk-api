---
UID: NF:midles.MesDecodeBufferHandleCreate
title: MesDecodeBufferHandleCreate function (midles.h)
description: The MesDecodeBufferHandleCreate function creates a decoding handle and initializes it for a (fixed) buffer style of serialization.
helpviewer_keywords: ["MesDecodeBufferHandleCreate","MesDecodeBufferHandleCreate function [RPC]","_rpc_mesdecodebufferhandlecreate","midles/MesDecodeBufferHandleCreate","rpc.mesdecodebufferhandlecreate"]
old-location: rpc\mesdecodebufferhandlecreate.htm
tech.root: Rpc
ms.assetid: 10a2312d-5969-4dde-bf62-308ad425569b
ms.date: 12/05/2018
ms.keywords: MesDecodeBufferHandleCreate, MesDecodeBufferHandleCreate function [RPC], _rpc_mesdecodebufferhandlecreate, midles/MesDecodeBufferHandleCreate, rpc.mesdecodebufferhandlecreate
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
 - MesDecodeBufferHandleCreate
 - midles/MesDecodeBufferHandleCreate
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
 - MesDecodeBufferHandleCreate
---

# MesDecodeBufferHandleCreate function


## -description

The 
<b>MesDecodeBufferHandleCreate</b> function creates a decoding handle and initializes it for a (fixed) buffer style of serialization.

## -parameters

### -param Buffer

Pointer to the buffer containing the data to decode.

### -param BufferSize

Bytes of data to decode in the buffer.

### -param pHandle

Pointer to the address to which the handle will be written.

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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_INVALID_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer was not valid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>MesDecodeBufferHandleCreate</b> routine is used by applications to create a serialization handle and initialize the handle for the (fixed) buffer style of decoding. When using the fixed buffer style of decoding, the user supplies a single buffer containing all the encoded data. This buffer must have an address which is aligned at 8, and must be a multiple of 8 bytes in size. Further, it must be large enough to hold all of the data to decode.

## -see-also

<a href="/windows/desktop/api/midles/nf-midles-mesencodefixedbufferhandlecreate">MesEncodeFixedBufferHandleCreate</a>



<a href="/windows/desktop/api/midles/nf-midles-meshandlefree">MesHandleFree</a>